#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-privilege-assign-success-4672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [ """Special privileges assigned to new logon""", """Privileges""" ]
Fields = [
  """\d\d:\d\d:\d\d(\+|-)\d\d:\d\d ({host}[\w\-.]+)""",
  """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({host}[\w\-.]+)\s""",
  """"host":"(::ffff:)?({host}[\w\-.]+)"""",
  """({event_name}Special privileges assigned to new logon)""",
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z?)"""
  """TimeGenerated=({time}\d{10})"""
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """(::ffff:)?(({host}[\w\-.]+)\s+)?({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
  """\scategoryOutcome=(|/({result}[^=]+?))(\s+\w+=|\s*$)""",
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
  """({result}(?i)(((audit|success|failure)( |_)(success|audit|failure))|information))\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*""",
  """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)""",
  """(::ffff:)?({host}[\w\-.]+)\/Microsoft-Windows-Security-Auditing \(4672\)""",
  """"dhn":"(::ffff:)?({host}[\w\-.]+)""",
  """Type\s*=\s*"({result}[^";]+)"""",
  """Keywords=({result}[^=]+?);?\s*(\w+=)""",
  """<Computer>(::ffff:)?({src_host}({host}[\w\-.]+))</Computer>""",
  """Computer(\w+)?["\s]*(:|=)\s*"?(::ffff:)?({src_host}({host}[\w\-.]+))""",
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """({event_code}4672)""",
  """Account Name(:|=)\s*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\\r|\\n|\\t)*[\s;]*Account Domain(:|=)""",
  """Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*(\\[rnt])*\s*Logon ID(:|=)""",
  """\s*Logon ID(:|=)\s*({login_id}[^=]+?)[\s;]*Privileges(:|=)\s*({privileges}.+?)(<|\s*User:|\s+\d+|,|\s*\"|;|\s*$|\s*\(EventID)""",
  """sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """EVENT_TYPE="({result}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```