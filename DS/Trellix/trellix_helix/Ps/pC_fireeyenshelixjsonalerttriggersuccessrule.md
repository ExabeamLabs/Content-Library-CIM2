#### Parser Content
```Java
{
Name = "fireeye-nshelix-json-alert-trigger-success-rule"
Vendor = "Trellix"
Product = "Trellix Helix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
ExtractionType = json
Conditions = [
""""type":"fireeye_rule""""
""""threat_type":"""
""""category":"Host""""
]
Fields = [
"""exa_json_path=$.created_at,exa_field_name=time""",
"""exa_json_path=$.alert_type_details.detail.iocnames,exa_field_name=alert_name""",
"""exa_json_path=$.description,exa_field_name=additional_info""",
"""exa_regex=virus.+?"description":"({alert_name}[^"]+)"""",
"""exa_json_path=$.severity,exa_field_name=alert_severity""",
"""exa_json_path=$.threat_type,exa_field_name=alert_type""",
"""exa_json_path=$.alert_type_details.source,exa_regex=^({dest_host}[\w\-.]+)$""",
"""exa_json_path=$.alert_type_details.destination,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.alert_type_details.detail.username,exa_regex=^([\w\s]+\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
"""exa_json_path=$.alert_type_details.detail.process,exa_field_name=process_name""",
"""exa_json_path=$.alert_type_details.detail.processpath,exa_field_name=process_path""",
"""exa_regex="virus":"({malware_name}[^"]+)"""",
"""exa_json_path=$.alert_type_details.detail.result,exa_field_name=result""",
"""exa_json_path=$.alert_type_details.detail.filename,exa_regex=^({file_path}({file_dir}.*?)({file_name}[^\\\."]+(\.({file_ext}[^\\\."]+))?))$""",
"""exa_json_path=$.alert_type_details.detail.filename,exa_regex=^({file_name}[^\\\."]+(\.({file_ext}[^\\\."]+))?)$"""
"""exa_json_path=$.alert_type_details.detail.filepath,exa_regex=^({file_path}({file_dir}.*?)({file_name}[^\\\."]+(\.({file_ext}[^\\\."]+))?))$"""
]
ParserVersion = "v1.0.0"


}
```