#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-enable-success-4722"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "MM/dd/yyyy hh:mm:ss a", "MM/dd/yyyy HH:mm:ss", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
"""A user account was enabled"""
"""Account"""
"""Target"""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\""""
"""TimeGenerated=({time}\d{10})"""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""\"_raw\":\"({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
"""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
"""\s+(?i)(((audit|success)( |_)(success|audit))|information)\s+({host}[\w.\-]+)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s)"""
"""\"system_name\":\"({host}[^\"]+)\""""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""({event_code}4722)"""
"""Security(,|\srn=|\s+)({event_id}\d+)"""
"""\"TargetAccount\":\"(({dest_domain}[^\\\s\"]+)\\+)?({dest_user}[^\\\s\"]+)"""
"""Account Name:\s*\\?({user}[\w\.\-\!\#\^\~]{1,40}\$?)((?-i)\\+[rnt])*\s*Account Domain:\s*({domain}[^\s\\]+).+?Logon ID:\s*({login_id}[^\\\s]+)((?-i)\\+[rnt])*\s*Target.+?Account Name:\s*({dest_user}[^\\\s]+)((?-i)\\+[rnt])*\s*Account Domain:\s*({dest_domain}[^\s\"]+)"""
"""Account Name:(\\t|\\r|\\n|\s)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*({domain}[^\s"\\]+)(\\t|\\r|\\n|\s)*Logon ID:(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*Target.+?Account Name:(\\t|\\r|\\n|\s)*({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*({dest_domain}[^\s\\"]+)(\\t|\\r|\\n|\s)*"""
"""\"Account\":\"(({domain}[^\\\s\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\"SubjectLogonId\":\"({login_id}[^\s\"]+)"""
"""({time}\d\d\/\d\d\/\d\d\d\d\s*\d\d:\d\d:\d\d)"""
"""Target Account.+?Account Name:\s*(\\t|\\r|\\n|\s)*({dest_user}[^:].+?)\s*(\\n|\\r\s\\t)*?[rnt\\]*?\s*Account Domain:\s*"""
]
ParserVersion = "v1.0.0"


}
```