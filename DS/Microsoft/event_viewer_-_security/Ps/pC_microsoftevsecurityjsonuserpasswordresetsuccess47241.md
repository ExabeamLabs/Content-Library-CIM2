#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-password-reset-success-4724-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""event_id":4724"""
"""Microsoft-Windows-Security-Auditing"""
"""An attempt was made to reset an account's password"""
]
Fields = [
"""exa_json_path=$..created,exa_field_name=time""",
"""exa_json_path=$.message,exa_regex=({event_name}An attempt was made to reset an account's password)""",
"""exa_regex="keywords"+:\["+({result}[^"]+)""",
"""exa_json_path=$..pid,exa_field_name=process_id""",
"""exa_json_path=$..thread.id,exa_field_name=thread_id""",
"""exa_json_path=$..TargetUserName,exa_regex=^(None|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$..TargetDomainName,exa_field_name=dest_domain""",
"""exa_json_path=$..TargetLogonId,exa_field_name=dest_login_id""",
"""exa_json_path=$..LogonType,exa_field_name=login_type""",
"""exa_json_path=$..TargetSid,exa_field_name=dest_user_sid""",
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
"""exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```