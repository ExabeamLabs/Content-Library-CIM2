#### Parser Content
```Java
{
Name = gitlab-gl-json-app-activity-success-entity
  Vendor = GitLab
  Product = GitLab
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"entity_type":""", """"target_details":""", """"event_name":""", """"event_type":""", """"entity_path":""" ]
  Fields = [
    """exa_json_path=$.id,exa_field_name=event_id""",
    """exa_json_path=$.created_at,exa_field_name=time"""
    """exa_json_path=$.entity_type,exa_field_name=entity_type""",
    """exa_json_path=$.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.author_name,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.entity_path,exa_field_name=process_path""",
    """exa_json_path=$.target_details,exa_field_name=operation_details""",
    """exa_json_path=$.target_type,exa_field_name=operation"""
    """exa_json_path=$.event_type,exa_field_name=event_name""",
    """exa_json_path=$.details.event_name,exa_field_name=event_name""",
    """exa_json_path=$.details.author_name,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.details.author_class,exa_field_name=class_name""",
    """exa_json_path=$.details.target_type,exa_field_name=operation""",
    """exa_json_path=$.details.target_details,exa_field_name=operation_details""",
    """exa_json_path=$.details.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.details.entity_path,exa_field_name=process_path""",
    """exa_json_path=$.details.custom_message,exa_field_name=additional_info""",
    """exa_json_path=$.details.custom_message.protocol,exa_field_name=protocol"""
    """exa_json_path=$.details.custom_message.action,exa_field_name=action"""
  ]
  ParserVersion = "v1.0.0"  


}
```