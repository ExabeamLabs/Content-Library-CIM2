#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-lock-success-4800"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<EventID>4800"""
"""The workstation was locked"""
]
Fields = [
"""<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)"""
"""<Computer>({host}[^<]+)"""
"""({event_name}The workstation was locked)"""
"""({event_code}4800)"""
"""Data Name(\\)?='TargetUserName'>({user}[^<]+)"""
"""Data Name(\\)?='TargetDomainName'>({domain}[^<]+)"""
"""Data Name(\\)?='TargetLogonId'>({login_id}[^<]+)"""
"""Data Name(\\)?='TargetUserSid'>({user_sid}[^<]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```