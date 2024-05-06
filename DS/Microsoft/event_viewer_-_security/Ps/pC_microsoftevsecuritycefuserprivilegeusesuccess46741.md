#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-4674-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
Conditions = [
  """An operation was attempted on a privileged object."""
  """<EventID>4674</EventID>"""
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)""",
  """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)('|")/>""",
  """<Keywords>({result}[^<]+?)</Keywords>""",
  """<Computer>({host}({dest_host}[\w\-.]+))</Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """({event_code}4674)""",
  """Process Name:\s*((?-i)\\+[rnt])*(?:( |((?-i)\\+[rnt])*)|({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/"]+?)))[\\rnt\s]*Requested""",
  """Account Name:\s*[\\trn]*(?:-|({user}[\w\.\-]{1,40}\$?))[\\rnt\s]*Account Domain:""",
  """Account Domain:\s*[\\trn]*({domain}[^:]+?)[\\rnt\s]*Logon ID:""",
  """Logon ID:\s*((?-i)\\+[rnt])*({login_id}[^:]+?)[\\rnt\s]*Object:""",
  """Object Server:\s*((?-i)\\+[rnt])*({object_server}[^:]+?)[\\rnt\s]*Object Type:""",
  """Object Type:\s*((?-i)\\+[rnt])*(?:-|({object_type}[^:]+?))[\\rnt\s]*Object Name:""",
  """Object Name:\s*((?-i)\\+[rnt])*(?:|-|({object}[^<>]+?))[\\rnt\s]*Object Handle""",
  """Desired Access:\s*((?-i)\\+[rnt])*({access}[^:]+?)[\\rnt\s]*Privileges:""",
  """Privileges:\s*((?-i)\\+[rnt])*({privileges}[^:<>"=]+?)(\s*<|\s*($|")|\s*\w+=)"""
]
ParserVersion = "v1.0.0"


}
```