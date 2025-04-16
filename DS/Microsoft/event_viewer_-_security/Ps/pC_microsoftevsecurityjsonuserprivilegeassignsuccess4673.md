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
  """"Hostname":"({host}[\w\-.]*)""",
  """({event_code}4673)""",
  """"EventType":"({result}[^"]*)""",
  """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  """"SubjectDomainName":"({domain}[^"]*)""",
  """"SubjectLogonId":"({login_id}[^"]*)""",
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))",""",
  """"ObjectServer":"({object_server}[^"]*)""",
  """"PrivilegeList":"({privileges}[^"]*)"""
]
DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
ParserVersion = "v1.0.0"


}
```