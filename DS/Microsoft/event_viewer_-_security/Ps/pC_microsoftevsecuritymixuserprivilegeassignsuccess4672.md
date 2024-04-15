#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [ """Special privileges assigned to new logon""", """Privileges""" ]
Fields = [
  """\d\d:\d\d:\d\d(\+|-)\d\d:\d\d ({host}[^\s]+)""",
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({host}[\w\-.]+)\s""",
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))\s""",
  """"host":"(::ffff:)?({host}[^"]+)"""",
  """({event_name}Special privileges assigned to new logon)""",
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """(::ffff:)?({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
  """\scategoryOutcome=(|/({result}[^=]+?))(\s+\w+=|\s*$)""",
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
  """({result}(?i)(((audit|success|failure)( |_)(success|audit|failure))|information))\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*""",
  """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)""",
  """(::ffff:)?({host}[^\s\/]+)\/Microsoft-Windows-Security-Auditing \(4672\)""",
  """"dhn":"(::ffff:)?({host}[^-"]+)""",
  """Type\s*=\s*"({result}[^";]+)"""",
  """Keywords=({result}[^=]+?);?\s*(\w+=)""",
  """<Computer>(::ffff:)?({host}[^<]+)</Computer>""",
  """Computer(\w+)?["\s]*(:|=)\s*"?(::ffff:)?({host}[^\s";]+)""",
  """({event_code}4672)""",
  """Account Name(:|=)\s*(-|SYSTEM|({user}[^\s]+?))[\s;]*Account Domain(:|=)""",
  """Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)""",
  """\s*Logon ID(:|=)\s*({login_id}[^=]+?)[\s;]*Privileges(:|=)\s*({privileges}.+?)(<|\s*User:|\s+\d+|,|\s*\"|;|\s*$|\s*\(EventID)""",
  """sourceip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """EVENT_TYPE="({result}[^"]+)""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```