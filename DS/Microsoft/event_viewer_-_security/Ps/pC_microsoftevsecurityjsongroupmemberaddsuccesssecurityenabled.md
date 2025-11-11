#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-group-member-add-success-securityenabled"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""event_id":"""
"""Microsoft-Windows-Security-Auditing"""
"""A member was added to a security-enabled"""
]
Fields = [
"""exa_json_path=$..created,exa_field_name=time""",
"""exa_json_path=$.message,exa_regex=({event_name}An account was logged off)""",
"""exa_regex="keywords"+:\["+({result}[^"]+)""",
"""exa_json_path=$..pid,exa_field_name=process_id""",
"""exa_json_path=$..thread.id,exa_field_name=thread_id""",
"""exa_json_path=$..TargetUserName,exa_regex=^(None|({dest_user}[^"]+))$""",
"""exa_json_path=$..TargetDomainName,exa_field_name=dest_domain""",
"""exa_json_path=$..record_id,exa_field_name=event_id""",
"""exa_json_path=$..task,exa_field_name=task_name""",
"""exa_json_path=$..event_id,exa_field_name=event_code""",
"""exa_json_path=$..computer_name,exa_regex=^({src_host}[\w\-.]+)$""",
"""exa_json_path=$.host.hostname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$..action,exa_field_name=action""",
"""exa_json_path=$..os.name,exa_field_name=os""",
"""exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
"""exa_json_path=$..activity_id,exa_field_name=activity_id""",
"""exa_json_path=$..provider_name,exa_field_name=provider_name""",
"""exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
"""exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$..SubjectDomainName,exa_field_name=src_domain""",
"""exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
"""exa_json_path=$..PrivilegeList,exa_field_name=privileges,exa_match_expr=!InList($..PrivilegeList,"-")""",
"""exa_json_path=$.message,exa_regex=({event_name}A member was added to a security-enabled)""",
"""exa_regex="MemberSid":"(({dest_user_sid}S-\d+-[^"]+)|({account_id}[^"]+))"""",
"""exa_json_path=$..TargetSid,exa_field_name=group_id"""
]
ParserVersion = "v1.0.0"


}
```