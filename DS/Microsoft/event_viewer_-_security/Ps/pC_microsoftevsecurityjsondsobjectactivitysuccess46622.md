#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-activity-success-4662-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [ """"event_id":4662""", """An operation was performed on an object""", """"ObjectName":""", """"computer_name":""" ]
Fields = [
"""exa_json_path=$.message,exa_regex=({event_name}An operation was performed on an object)""",
"""exa_json_path=$.@timestamp,exa_field_name=time""",
"""exa_json_path=$.computer_name,exa_regex=^({host}[\w\-.]+?)$""",
"""exa_json_path=$.event_data.ObjectServer,exa_field_name=object_server""",
"""exa_json_path=$.event_data.ObjectName,exa_field_name=object_name""",
"""exa_json_path=$.event_data.ObjectType,exa_field_name=object_type""",
"""exa_json_path=$.event_data.SubjectUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.event_data.SubjectLogonId,exa_field_name=login_id""",
"""exa_json_path=$.event_data.SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$.event_data.OperationType,exa_field_name=action""",
"""exa_json_path=$.event_data.Properties,exa_field_name=properties""",
"""exa_json_path=$.event_data.AdditionalInfo,exa_field_name=attribute,exa_match_expr=!InList($.event_data.AdditionalInfo,"-")""",
"""exa_regex="keywords"+:\["+({result}[^"]+)""",
"""exa_json_path=$.event_id,exa_field_name=event_code""",
"""exa_json_path=$.event_data.AccessList,exa_field_name=access"""
]
DupFields = [ "object_name->object" ]
ParserVersion = "v1.0.0"


}
```