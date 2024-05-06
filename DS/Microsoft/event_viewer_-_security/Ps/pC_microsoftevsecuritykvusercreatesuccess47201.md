#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-create-success-4720-1"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
"""A user account was created"""
  ]
  Fields = [
"""TimeGenerated=({time}\d{10})"""
"""EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
"""({event_name}A user account was created)""",
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
"""({event_code}4720)""",
"""Hostname\":\"({host}[\w\-.]+)\"""",
""""ComputerName":"({host}[\w\-.]+)""",
"""(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(,|\s+)ComputerName =({host}[\w.\-]+)""",
"""({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing \(4720\)""",
"""\"dhn\":\"({host}[^-\"]+)""",
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}[\w\-.]+?)(\"|\s)""",
"""\"system_name\":\"({host}[\w\-.]+)\"""",
"""Security(,|\srn=|\s+)({event_id}\d+)""",
"""Account Name:\s+({user}[\w\.\-]{1,40}\$?).+?Account Domain:\s+({domain}[\w\-\.]+).+?Logon ID:\s+({login_id}[\w\-\.]+).+?Account Name:\s+({account_name}[\w\-\.]+).+?Account Domain:\s+({account_domain}[\w\.\-]+).+?Attributes""",
"""Subject:.+?Security ID:\s+({user_sid}[^\s]+).+?Account Name:\s+({user}[\w\.\-]{1,40}\$?).+?Account Domain:\s+({domain}[\w\-\.]+).+?Logon ID:\s+({login_id}[\w\-\.]+).*?New Account""",
"""New Account:.+?Security ID:\s+({account_id}[^\s]+)\s+Account Name:\s+({account_name}[\w.'\-]+).+?Account Domain:\s+({account_domain}[\w.\-]+)""",
"""Account Name:\s*(\\t|\\r|\\n)*({user}[\w\.\-]{1,40}\$?)\s*.+?Account Domain:\s*(\\t|\\r|\\n)*({domain}[\w\-\.]+).+?Logon ID:\s*(\\t|\\r|\\n)*({login_id}[\w\-\.]+).+?Account Name:\s*(\\t|\\r|\\n)*({account_name}[\w\-\.]+).+?Account Domain:\s*(\\t|\\r|\\n)*({account_domain}[\w\.\-]+).+?Attributes"""
"""(Enabled.+?|Account Control:)\s*'({user_type}.*?)'\s-\sEnabled"""
  ]
  DupFields = ["account_name->dest_user"]


}
```