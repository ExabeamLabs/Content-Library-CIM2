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
"""({event_name}A user account was locked out)"""
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[\w\-.]+)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<EventID>({event_code}[^<]+)</EventID>"""
"""<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>"""
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name\\*=('|")TargetUserName('|")>(?=\w)({account}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
"""<Data Name =('|")TargetDomainName('|")>(?:\\+)?({src_host}[\w\-\.]+)</Data>"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```