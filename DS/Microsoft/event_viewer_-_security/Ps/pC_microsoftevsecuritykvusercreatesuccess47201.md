#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-create-success-4720-1"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
"""A user account was created"""
  ]
  Fields = [
"""EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
"""({event_name}A user account was created)""",
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
"""({event_code}4720)""",
"""Hostname\":\"({host}[^\"]+)\"""",
"""(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(,|\s+)({host}[\w.\-]+),?""",
"""({host}[^\/\s]+)\/Microsoft-Windows-Security-Auditing \(4720\)""",
"""\"dhn\":\"({host}[^-\"]+)""",
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s)""",
"""\"system_name\":\"({host}[^\"]+)\"""",
"""Security(,|\srn=|\s+)({event_id}\d+)""",
"""Account Name:\s+({user}[\w\-\.]+).+?Account Domain:\s+({domain}[\w\-\.]+).+?Logon ID:\s+({login_id}[\w\-\.]+).+?Account Name:\s+({account_name}[\w\-\.]+).+?Account Domain:\s+({account_domain}[\w\.\-]+).+?Attributes""",
"""Subject:.+?Security ID:\s+({user_sid}[^\s]+).+?Account Name:\s+({user}[\w\.\-]+).+?Account Domain:\s+({domain}[\w\-\.]+).+?Logon ID:\s+({login_id}[\w\-\.]+).*?New Account""",
"""New Account:.+?Security ID:\s+({account_id}[^\s]+)\s+Account Name:\s+({account_name}[\w.'\-]+).+?Account Domain:\s+({account_domain}[\w.\-]+)""",
"""Enabled.*?'({user_type}[^']+)"""
  ]
  DupFields = ["host->dest_host" ]


}
```