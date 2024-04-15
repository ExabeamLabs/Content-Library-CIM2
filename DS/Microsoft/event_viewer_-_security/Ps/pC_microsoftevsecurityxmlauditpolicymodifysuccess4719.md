#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-audit-policy-modify-success-4719"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4719<"""
"""<Data Name ='SubjectUserName'>"""
]
Fields = [
"""({event_code}4719)"""
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)"""
"""<Computer>(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^<]+))"""
"""<Data Name ='SubjectUserSid'>({user_sid}[^<]+)"""
"""<Data Name ='SubjectUserName'>({user}[^<]+)"""
"""<Data Name ='SubjectDomainName'>({domain}[^<]+)"""
"""<Data Name ='SubjectLogonId'>({login_id}[^<]+)"""
"""<Data Name ='CategoryId'>({category_id}[^<]+)"""
"""<Data Name ='SubcategoryId'>({sub_category_id}[^<]+)"""
"""<Data Name ='AuditPolicyChanges'>({audit_policy_name}[^<]+)"""
"""<Message>({event_name}System audit policy was changed)"""
]
ParserVersion = "v1.0.0"


}
```