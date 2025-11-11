#### Parser Content
```Java
{
Name = "pan-cortex-json-alert-trigger-success-xdr"
Vendor = "Palo Alto Networks"
Product = "Cortex XDR"
TimeFormat = "epoch"
ExtractionType = json 
Conditions = [ """"event_type":""", """"alert_type":""", """"alert_id":""", """"severity":""", """"source":""" ]
Fields = [
"""exa_json_path=$.event_timestamp,exa_field_name=time""",
"""exa_json_path=$.event_id,exa_field_name=event_id""",
"""exa_json_path=$.source,exa_field_name=log_source""",
"""exa_json_path=$.host_name,exa_field_name=host""",
"""exa_json_path=$.category,exa_field_name=category"""
"""exa_json_path=$.severity,exa_field_name=alert_severity""",
"""exa_json_path=$..description,exa_field_name=description"""
"""exa_regex=user_name":\["(({domain}[^\\"]+)\\\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
"""exa_json_path=$.agent_os_type,exa_field_name=os"""
"""exa_json_path=$.action,exa_field_name=action""",
"""exa_json_path=$.event_type,exa_field_name=event_category""",
"""exa_json_path=$.causality_actor_process_image_name,exa_field_name=image_name"""
"""exa_json_path=$.causality_actor_process_signature_status,exa_field_name=file_signature_status"""
"""exa_json_path=$.causality_actor_process_image_md5,exa_field_name=hash_md5"""
"""exa_json_path=$.action_local_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.action_remote_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```