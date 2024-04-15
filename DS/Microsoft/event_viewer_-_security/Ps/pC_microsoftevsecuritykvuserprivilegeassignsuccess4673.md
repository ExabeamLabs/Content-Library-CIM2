#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-assign-success-4673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [ """A privileged service was called""", """Privileges""" ]
Fields = [
  """({event_name}A privileged service was called)""",
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({host}[\w\-.]+)\s""",
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))\s""",
  """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
  """({result}(?i)(((audit|success|failure)( |_)(success|audit|failure))|information))\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*""",
  """({host}[\w.\-]+)\s*:\s+A privileged service was called""",
  """({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4673\)""",
  """"dhn":"({host}[^-"]+)""",
  """Event Type\s*:\s*({result}.+?)\.\s+Log Type""",
  """Type\s*=\s*"({result}[^";]+)"""",
  """Keywords=({result}.+?);?\s*Message=""",
  """<Computer>({host}[^<]+)</Computer>""",
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s|;)""",
  """\s*Source Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Source Port(:|=)""",
  """({event_code}4673)""",
  """Process Name(:|=)\s*(?: |({process_path}({process_dir}(\w+:)(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Service Request Information(:|=)""",
  """\s*Account Name(:|=)\s*({user}.+?)[\s;]*Account Domain(:|=)""",
  """\s*Account Domain(:|=)\s*({domain}.+?)[\s;]*Logon ID(:|=)""",
  """\s*Logon ID(:|=)\s*({login_id}.+?)[\s;]*Service(:|=)""",
  """\s*Server(:|=)\s*({object_server}.+?)[\s;]*Service Name""",
  """\s*Privileges(:|=)\s*({privileges}.+?)(\s*$|\s+\d+|"|,|;)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```