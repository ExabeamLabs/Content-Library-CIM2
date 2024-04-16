#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-audit-policy-modify-success-4719"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4719<"""
"""<Data Name"""
"""SubjectUserName"""
]
Fields = [
"""({event_code}4719)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Computer>(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[\w\-.]+))"""
"""<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)"""
"""<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-]{1,40}\$?))"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)"""
"""<Data Name\\*=('|")CategoryId('|")>({category_id}[^<]+)"""
"""<Data Name\\*=('|")SubcategoryId('|")>({sub_category_id}[^<]+)"""
"""<Data Name\\*=('|")AuditPolicyChanges('|")>({result}[^<]+)"""
"""<Message>({event_name}System audit policy was changed)"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```