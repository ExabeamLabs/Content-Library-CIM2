#### Parser Content
```Java
{
Name = "arcticwolf-protect-json-alert-trigger-success-memoryprotection"
Vendor = "Arctic Wolf"
Product = "Cylance Protect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [
"""destinationServiceName =Cylance Protect"""
"""dproc=memoryProtection"""
""""device_id":"""
"""event_id":""""
]
Fields = [
    """exa_json_path=$.process_id,exa_field_name=process_id"""
    """exa_json_path=$.device_id,exa_field_name=device_id"""
    """exa_json_path=$.user_name,exa_regex=(null|-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.created,exa_field_name=time"""
    """exa_json_path=$.agent_event_id,exa_field_name=alert_id"""
    """exa_json_path=$.groups,exa_field_name=group_name"""
    """exa_json_path=$.sid,exa_field_name=user_sid"""
    """exa_json_path=$.image_name,exa_regex=({file_path}({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s"]+))?))("|$)"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.device_image_file_event_id,exa_field_name=device_id"""
    """exa_json_path=$.file_hash_id,exa_field_name=hash_sha256"""
]
ParserVersion = "v1.0.0"


}
```