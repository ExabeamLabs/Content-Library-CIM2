#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-use-success-4673
    Vendor = Microsoft
    Product = Event Viewer - Security 
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """"EventID":"4673"""", """<Data Name ='""" ]
    Fields = [
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"Computer":"({host}[^"]+)""",
      """"EventID":"({event_code}\d+)""",
      """<Data Name ='SubjectUserSid'>\s*(({domain}[^\\]+)\\)?({user}[^<]+)</Data>""",
      """<Data Name ='SubjectUserName'>({user}[^<]+?)</Data>""",
      """<Data Name ='SubjectDomainName'>({domain}[^<]+?)</Data>""",
      """<Data Name ='SubjectLogonId'>({login_id}[^<]+?)</Data>""",
      """<Data Name ='ObjectServer'>({object_server}[^<]+?)</Data>""",
      """<Data Name ='PrivilegeList'>({privileges}[^<]+?)</Data>""",
      """<Data Name ='ProcessName'>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))</Data>""",
    ]
    DupFields = ["host->dest_host"]
  

}
```