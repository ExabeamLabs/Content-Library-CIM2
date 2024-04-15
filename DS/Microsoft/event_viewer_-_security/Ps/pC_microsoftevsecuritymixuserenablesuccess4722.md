#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-enable-success-4722"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""A user account was enabled"""
"""Account"""
"""Target"""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\""""
"""({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
"""\"_raw\":\"({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))"""
"""\s+(?i)(((audit|success)( |_)(success|audit))|information)\s+({host}[\w.\-]+)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s)"""
"""\"system_name\":\"({host}[^\"]+)\""""
"""({event_code}4722)"""
"""Security(,|\srn=|\s+)({event_id}\d+)"""
"""Account Name:\s*\\?({user}[^\s]+)\s*Account Domain:\s*({domain}[^\s]+).+?Logon ID:\s*({login_id}[^\s]+)\s*Target.+?Account Name:\s*({dest_user}[^\s]+)\s*Account Domain:\s*({dest_domain}[^\s\"]+)"""
"""\"Account\":\"(({domain}[^\\\s\"]+)\\+)?({user}[^\\\s\"]+)"""
"""\"TargetAccount\":\"(({dest_domain}[^\\\s\"]+)\\+)?({dest_user}[^\\\s\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\s\"]+)"""
]
ParserVersion = "v1.0.0"


}
```