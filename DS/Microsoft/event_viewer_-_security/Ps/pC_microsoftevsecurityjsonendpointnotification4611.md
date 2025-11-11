#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-4611
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """EventID":4611""", """A trusted logon process has been registered with the Local Security Authority""",""""Channel":"Security"""" ]
    Fields = [
      """"+EventTime"+:\s*"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})"+""",
      """"+(Hostname|Computer)"+:"+({host}[^"]+)"+""",
      """"+EventType"+:"+({result}[^"]+)"+""",
      """"+SourceName"+:"+({log_source}[^"]+)"+""",
      """"+ProcessID"+:({process_id}\d+)""",
      """"+ThreadID"+:({thread_id}\d+)""",
      """"+Message"+:"+({additional_info}[^"]+?)\s*Subject:""",
      """"+Category"+:"+({category}[^"]+)"+""",
      """"+ActivityID"+:"+\{({activity_id}[^}]+)""",
      """"+EventID"+:({event_code}\d+)""",
      """"SubjectLogonId"+:"+({login_id}[^"]+)"""",
      """"LogonProcessName"+:"+({process_name}[^"]+)"""",
      """"SubjectUserSid"+:"+({user_sid}[^"]+)"""",
      """"SubjectUserName"+:"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """({event_name}A trusted logon process has been registered with the Local Security Authority)"""
    ]
  

}
```