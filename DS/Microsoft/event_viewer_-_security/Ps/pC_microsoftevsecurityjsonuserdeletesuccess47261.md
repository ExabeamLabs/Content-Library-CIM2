#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-delete-success-4726-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ExtractionType = json
Conditions = [
""""EventID":4726"""
"""SubjectUserSid":"""
"""A user account was deleted"""
]
Fields = [
"""exa_json_path=$.EventTime,exa_field_name=time""",
"""exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$.Message,exa_regex=({event_name}A user account was deleted)""",
"""exa_json_path=$.TargetUserName,exa_regex=^({account_name}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$.TargetDomainName,exa_field_name=dest_domain""",
"""exa_json_path=$.TargetSid,exa_field_name=dest_user_sid""",
"""exa_json_path=$.EventID,exa_field_name=event_code""",
"""exa_json_path=$.SubjectUserSid,exa_field_name=user_sid""",
"""exa_json_path=$.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$.SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$.SubjectDomainName,exa_field_name=src_domain""",
"""exa_json_path=$.SubjectLogonId,exa_field_name=login_id"""
]
ParserVersion = "v1.0.0"


}
```