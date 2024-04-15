#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-4738"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4738<"""
]
Fields = [
"""<EventID>({event_code}\d+)"""
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Message>({event_name}A user account was changed)"""
"""<Computer>({host}[^<]+)"""
"""<Data Name ='SubjectUserSid'>({user_sid}[^<]+)"""
"""<Data Name ='SubjectUserName'>({user}[^<]+)"""
"""<Data Name ='SubjectDomainName'>({domain}[^<]+)"""
"""<Data Name ='TargetUserName'>({dest_user}[^<]+)"""
"""<Data Name ='TargetDomainName'>({dest_domain}[^<]+)"""
"""<Data Name ='TargetSid'>({dest_user_sid}[^<]+)"""
"""<Data Name ='SubjectLogonId'>({login_id}[^<]+)"""
"""<Data Name ='OldUacValue'>({old_attribute}[^<]+)"""
"""<Data Name ='NewUacValue'>({new_attribute}[^<]+)"""
"""Changed Attributes:\s*(|({attribute}[^:]+?))\s+SAM Account Name:"""
"""User Account Control:\s*(-|({uac_status}[^:]+?))\s*User Parameters:"""
]
ParserVersion = "v1.0.0"


}
```