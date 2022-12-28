#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":"""
"""4740"""
"""A user account was locked out"""
]
Fields = [
"""({event_name}A user account was locked out)"""
"""\"EventTime\":\s*\"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
"""\"Hostname\":\"({host}[\w\-.]+)"""
"""({event_code}4740)"""
"""\"SubjectUserName\":\"({src_user}[^\"]+)"""
"""\"SubjectDomainName\":\"({src_domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"TargetSid\":\"({user_sid}[^\"]+)"""
"""\"TargetUserName\":\"({user}[^\"]+)"""
"""Additional Information:[\\rnt]*Caller Computer Name:[\\rnt]*({src_host}[^\"]+)"""
]
DupFields = [
"host->dest_host"
"src_domain->domain"
]
ParserVersion = "v1.0.0"


}
```