#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-4688wls
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LogType="WLS"""", """EventID="4688"""" ]
    Fields = [
      """Computer="+({host}[\w\-.]+)"""",
      """EventID="+({event_code}[^"]+)"""",
      """NewProcessName ="+({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+))"""",
      """NewProcessName ="+({path}.+?)"""",
      """SubjectUserName ="+(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """SubjectDomainName ="+(?=\w)({src_domain}({domain}[^"]+))"""",
      """SubjectLogonId="+({login_id}[^"]+)"""",
      """ProcessId="+({parent_process_guid}[^"]+)"""",
      """ProviderGuid="+({process_guid}[^"]+)"""",
      """SubjectUserSid="+({user_sid}[^"]+)"""",
      """NewProcessId="+({process_id}[^"]+)"""",
      """CommandLine="+({process_command_line}[^"]+)"""",
      """CommandLine="+(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= ({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+))""",
    ]
  

}
```