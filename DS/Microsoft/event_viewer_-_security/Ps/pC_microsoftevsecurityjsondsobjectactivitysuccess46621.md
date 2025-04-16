#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-activity-success-4662-1"
Conditions = [
""""EventID":"4662""""
"""An operation was performed on an object"""
]
ExtractionType = json
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss" ]
Fields = [
"""exa_json_path=$.TimeCreated,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""exa_json_path=$.TimeCreated,exa_field_name=time""",
"""exa_json_path=$.Message,exa_regex=({event_name}An operation was performed on an object)""",
"""exa_json_path=$.Keywords,exa_field_name=result""",
"""exa_json_path=$..ProcessID,exa_field_name=process_id""",
"""exa_json_path=$..ThreadID,exa_field_name=thread_id""",
"""exa_json_path=$.EventRecordID,exa_field_name=event_id""",
"""exa_json_path=$.Task,exa_field_name=task_name""",
"""exa_json_path=$.EventID,exa_field_name=event_code""",
"""exa_json_path=$.Computer,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
"""exa_json_path=$.Provider.Name,exa_field_name=provider_name""",
"""exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
"""exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$..ObjectName,exa_field_name=object_name""",
"""exa_json_path=$..ObjectServer,exa_field_name=object_server""",
"""exa_json_path=$..ObjectType,exa_field_name=object_type""",
"""exa_json_path=$..OperationType,exa_field_name=operation""",
"""exa_json_path=$..AdditionalInfo,exa_regex=(?:-|({additional_info}[^"]+))""",
"""exa_json_path=$..AccessList,exa_field_name=access""",
"""exa_regex=Accesses:(\\[srnt])*(-|({access}[^:]+?))(\\[srnt])*Access Mask:"""
]
DupFields = ["object_name->object", "user->src_user", "domain->src_domain"]


}
```