#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-unlock-success-4767
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4767</EventID>"""
"""<Event xmlns="""
]
Fields = [
"""({event_name}A user account was unlocked)"""
"""<Computer>({host}[\w\-.]+?)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Data Name\\*=('|")SubjectLogonId('|")>\s*({login_id}.+?)\s*</Data>"""
"""<Data Name\\*=('|")SubjectUserName('|")>\s*((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*</Data>"""
"""<Data Name\\*=('|")SubjectDomainName('|")>\s*({domain}[^\s]+?)\s*</Data>"""
"""<Data Name\\*=('|")SubjectUserSid('|")>\s*({user_sid}[^\s]+?)\s*</Data>"""
"""<Data Name\\*=('|")TargetDomainName('|")>\s*({dest_domain}[^\s]+?)\s*</Data>"""
"""<Data Name\\*=('|")TargetUserName('|")>\s*({dest_user}[^\s]+?)\s*</Data>"""
"""<Data Name\\*=('|")TargetSid('|")>\s*({dest_user_sid}.+?)</Data>\s*"""
"""({event_code}4767)"""
"""<Level>({run_level}[^<]+)<"""
  ]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```