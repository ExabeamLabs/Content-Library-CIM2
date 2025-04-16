#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-disable-success-4725-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4725"""
""""SourceModuleType":"""
]
Fields = [
"""({event_name}A user account was disabled)"""
"""\"EventTime\":\s*\"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
"""\"Hostname\":\"({host}[\w\-.]*)"""
"""({event_code}4725)"""
"""\"SubjectUserSid\":\"({user_sid}[^\"]+)"""
"""\"SubjectUserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\"SubjectDomainName\":\"({domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"TargetSid\":\"({dest_user_sid}[^\"]+)"""
"""\"TargetUserName\":\"({dest_user}[^\"]+)"""
"""\"TargetDomainName\":\"({dest_domain}[^\"]+)"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```