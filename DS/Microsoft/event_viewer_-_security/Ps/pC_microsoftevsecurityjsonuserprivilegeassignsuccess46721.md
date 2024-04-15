#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-assign-success-4672-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4672</EventID>"""
  """Special privileges assigned to new logon"""
  """logon.Subject:"""
]
Fields = [
  """({event_name}Special privileges assigned to new logon)"""
  """\WSystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>({host}[\w\-\.]+)</Computer>"""
  """<Keywords>({action}[^<]+)</Keywords>"""
  """<EventID>({event_code}[^<]+)</EventID>"""
  """\s*Account Name:\s*({user}.+?)\s*Account Domain:\s*({domain}[^\s]+)\s*Logon ID:"""
  """\s*Logon ID:\s*({login_id}.+?)\s*Privileges:"""
  """\s*Privileges:\s*({privileges}.+?)</EventData>"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```