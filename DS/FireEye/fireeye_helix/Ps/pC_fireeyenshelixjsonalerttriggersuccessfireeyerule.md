#### Parser Content
```Java
{
Name = "fireeye-nshelix-json-alert-trigger-success-fireeyerule"
Vendor = "FireEye"
Product = "FireEye Helix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""type":"fireeye_rule""""
""""threat_type":"""
""""category":"Network""""
]
Fields = [
"""exa_json_path=$.created_at,exa_field_name=time""",
"""exa_json_path=$.message,exa_field_name=alert_name""",
"""exa_json_path=$.severity,exa_field_name=alert_severity""",
"""exa_json_path=$.threat_type,exa_field_name=alert_type""",
"""exa_json_path=$.alert_type_details.source,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
"""exa_json_path=$.alert_type_details.destination,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.protocol,exa_field_name=protocol""",
"""exa_json_path=$.alert_type_details.detail.domain,exa_field_name=domain""",
"""exa_json_path=$.created_by.username,exa_regex=^(system_user|({user}[\w\.\-]{1,40}\$?))$""",
"""exa_json_path=$.description,exa_field_name=additional_info"""
]
ParserVersion = "v1.0.0"


}
```