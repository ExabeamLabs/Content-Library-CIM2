#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-enable-success-4722"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4722</EventID>""",
"""TargetSid""",
"""TargetUserName""",
"""<Data Name""",
"""</Data>"""
]
Fields = [
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""({event_code}4722)"""
"""Subject:.+?Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:"""
"""Target Account:\s*Security ID:\s*({account_id}.+?)\s*Account Name:\s*(.+?)\s*Account Domain:\s*({dest_domain}.+?)\s*<"""
"""({event_name}A user account was enabled)"""
"""<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<"""
"""<Data Name\\*=('|")TargetUserName('|")>({dest_user}\S+)</Data>"""
"""<Data Name\\*=('|")TargetDomainName('|")>({dest_domain}[^<]+)<"""
"""<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))<"""
"""<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-]{1,40}\$?)<"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```