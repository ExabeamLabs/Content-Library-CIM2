#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-unlock-success-4801"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4801</EventID>""",
"""TargetUserName""",
"""<Data Name""",
"""</Data>"""
]
Fields = [
"""({event_name}The workstation was unlocked)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({dest_host}({host}[\w\-.]+))<"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<EventID>({event_code}4801)"""
"""Data Name(\\)?=('|")TargetUserName('|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Data Name(\\)?=('|")TargetDomainName('|")>({dest_domain}({domain}[^<]+))"""
"""Data Name(\\)?=('|")TargetLogonId('|")>({dest_login_id}({login_id}[^<]+))"""
"""Data Name(\\)?=('|")TargetUserSid('|")>({dest_user_sid}({user_sid}[^<]+))"""
"""<Level>({run_level}[^<]+)"""
]
ParserVersion = "v1.0.0"


}
```