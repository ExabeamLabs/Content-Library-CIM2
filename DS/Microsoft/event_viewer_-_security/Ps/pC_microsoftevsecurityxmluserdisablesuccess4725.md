#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-disable-success-4725"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4725</EventID>"""
"""<Data Name"""
"""TargetSid"""
]
Fields = [
"""({event_name}A user account was disabled)"""
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[\w\-.]+)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<EventID>({event_code}[^<]+)</EventID>"""
"""<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>"""
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))</Data>"""
"""<Data Name\\*=('|")TargetUserName('|")>(?=\w)({dest_user}[^<]+)</Data>"""
"""<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({dest_domain}[^<]+)</Data>"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```