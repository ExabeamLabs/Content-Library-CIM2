#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-unlock-success-4767
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ExtractionType = json
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4767"""
"""A user account was unlocked."""
""""Category""""
]
Fields = [
"""({event_name}A user account was unlocked)"""
"""\"EventTime\":\s*\"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
"""\"Hostname\":\"({host}[\w\-.]+)"""
"""({event_code}4767)"""
"""\"SubjectUserSid\":\"({user_sid}[^\"]+)"""
"""\"SubjectUserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\"SubjectDomainName\":\"({domain}[^\"]+)"""
"""\"SubjectLogonId\":\"({login_id}[^\"]+)"""
"""\"TargetDomainName\":\"({dest_domain}[^\"]+)"""
"""\"TargetUserName\":\"({dest_user}[^\"]+)"""
"""\"TargetSid\":\"({dest_user_sid}[^\"]+)"""
"""exa_regex=({event_name}A user account was unlocked)"""
"""exa_json_path=$.EventTime,exa_field_name=time"""
"""exa_json_path=$.Hostname,exa_field_name=host"""
"""exa_regex=({event_code}4767)"""
"""exa_json_path=$.SubjectUserSid,exa_field_name=user_sid"""
"""exa_json_path=$.SubjectUserName,exa_field_name=user"""
"""exa_json_path=$.SubjectDomainName,exa_field_name=domain"""
"""exa_json_path=$.SubjectLogonId,exa_field_name=login_id"""
"""exa_json_path=$.TargetDomainName,exa_field_name=dest_domain"""
"""exa_json_path=$.TargetUserName,exa_field_name=dest_user"""
"""exa_json_path=$.TargetSid,exa_field_name=dest_user_sid"""
]
DupFields = ["src_user->user", "src_domain->domain"]
ParserVersion = "v1.0.0"


}
```