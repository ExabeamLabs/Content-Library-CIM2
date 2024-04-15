#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-assign-success-4673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>4673</EventID>""", """A privileged service was called""", """Privileges:""" ]
Fields = [
  """({event_name}A privileged service was called)""",
  """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """({result}Information|Audit Success|Success Audit|Failure Audit|Audit Failure)""",
  """<Computer>({host}[^<]+)</Computer>""",
  """<EventID>({event_code}[^<]+)</EventID>""",
  """Process Name:\s*(?: |({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/"]+?)))\s*Service Request Information:""",
  """Account Name:\s*({user}[^=]+?)\s*Account Domain:""",
  """Account Domain:\s*({domain}[^=]+?)\s*Logon ID:""",
  """Logon ID:\s*({login_id}.+?)\s*Service:""",
  """Server:\s*({object_server}[^=]+?)\s*Service Name""",
  """Privileges:\s*({privileges}[^<>\s"=]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```