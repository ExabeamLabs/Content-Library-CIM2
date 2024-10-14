#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-enable-success-4722"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4722""""
""""SourceModuleType":""""
]
Fields = [
"""({event_name}A user account was enabled)"""
"""\"EventTime\":\s*\"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
"""\"Hostname\":\"({host}[^.\"]*)"""
"""({event_code}4722)"""
"""\"RecordNumber\":({event_id}[^,]+)"""
"""\"SubjectUserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\"SubjectDomainName\":\"({domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"TargetUserName\":\"({dest_user}[^\"]+)"""
"""\"TargetDomainName\":\"({dest_domain}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```