#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4740</EventID>"""
"""<Data Name""",
"""TargetSid"""
]
Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({dest_host}({host}[^<]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<EventID>({event_code}[^<]+)</EventID>"""
"""<Data Name\\*=('|")SubjectUserName('|")>({src_user}[^<]+)</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({src_domain}[^<]+)</Data>"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>"""
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name\\*=('|")TargetUserName('|")>(?=\w)({user}[^<]+)</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
"""<Data Name ='TargetDomainName'>({host}[\w\-\.]+)</Data>"""
]
ParserVersion = "v1.0.0"


}
```