#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-use-success-4673
    Vendor = Microsoft
    Product = Event Viewer - Security 
    ParserVersion = "v1.0.0"
    TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
    Conditions = [ """"EventID":"4673"""", """<Data Name""" ]
    Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{7}Z)""",
      """"Computer":"({host}[\w\-.]+)""",
      """"EventID":"({event_code}\d+)""",
      """<Data Name\\*='SubjectUserSid'>\s*(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
      """<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
      """<Data Name\\*='SubjectDomainName'>({domain}[^<]+?)</Data>""",
      """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+?)</Data>""",
      """<Data Name\\*='ObjectServer'>({object_server}[^<]+?)</Data>""",
      """<Data Name\\*='PrivilegeList'>({privileges}[^<]+?)</Data>""",
      """<Data Name\\*='ProcessName'>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))</Data>""",
      """"+SubjectUserSid"+:"+({user_sid}[^"<,]+)""",
      """"ProcessId":"({process_id}[^"]+)"""
      """({event_name}An account was logged off)""",
      """({event_name}A privileged service was called)"""
    ]
    DupFields = ["host->dest_host"]
  

}
```