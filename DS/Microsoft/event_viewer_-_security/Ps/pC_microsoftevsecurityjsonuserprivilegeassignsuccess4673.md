#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """"EventID":4673""", """"SourceModuleType":""" ]
Fields = [
  """({event_name}A privileged service was called)""",
  """"EventTime":\s*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})"""",
  """"Hostname":"({dest_host}({host}[\w\-.]*))""",
  """({event_code}4673)""",
  """"EventType":"({result}[^"]*)""",
  """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """"SubjectDomainName":"({src_domain}({domain}[^"]*))""",
  """"SubjectLogonId":"({login_id}[^"]*)""",
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))",""",
  """"ObjectServer":"({object_server}[^"]*)""",
  """"PrivilegeList":"({privileges}[^"]*)"""
]
ParserVersion = "v1.0.0"


}
```