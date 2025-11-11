#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-567-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""event_id":567,"""
"""Object Access Attempt:"""
]
Fields = [
"""exa_json_path=$.message,exa_regex=({event_name}Object Access Attempt)""",
"""exa_json_path=$.@timestamp,exa_field_name=time""",
"""exa_json_path=$.computer_name,exa_regex=^({dest_host}({host}[\w\-.]+))$""",
"""exa_json_path=$.record_number,exa_field_name=event_id""",
"""exa_json_path=$.event_id,exa_field_name=event_code""",
"""exa_json_path=$.user.identifier,exa_field_name=user_sid""",
"""exa_json_path=$.user.name,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.user.domain,exa_field_name=domain""",
"""exa_json_path=$..param3,exa_field_name=file_type""",
"""exa_json_path=$..ObjectType,exa_field_name=file_type""",
"""exa_json_path=$..param5,exa_regex=^({file_path}({file_dir}[^"]+?\\+)({file_name}[^\\\."]+(\.({file_ext}[^\.\\"]+))?))$""",
"""exa_json_path=$..ObjectName,exa_regex=^({file_path}({file_dir}[^"]+?\\+)({file_name}[^\\\."]+(\.({file_ext}[^\.\\"]+))?))$""",
"""exa_json_path=$..param6,exa_field_name=access""",
"""exa_json_path=$..Accesses,exa_field_name=access"""
]
ParserVersion = "v1.0.0"


}
```