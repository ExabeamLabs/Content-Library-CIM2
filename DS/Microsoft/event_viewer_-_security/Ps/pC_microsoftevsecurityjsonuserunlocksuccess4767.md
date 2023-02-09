#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-unlock-success-4767
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4767"""
"""A user account was unlocked."""
""""Category""""
]
Fields = [
"""({event_name}A user account was unlocked)"""
"""\"EventTime\":\s*\"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
"""\"Hostname\":\"({host}[^\"]+)"""
"""({event_code}4767)"""
"""\"SubjectUserSid\":\"({user_sid}[^\"]+)"""
"""\"SubjectUserName\":\"({user}[^\"]+)"""
"""\"SubjectDomainName\":\"({domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"TargetDomainName\":\"({dest_domain}[^\"]+)"""
"""\"TargetUserName\":\"({dest_user}[^\"]+)"""
"""\"TargetSid\":\"({dest_user_sid}[^\"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```