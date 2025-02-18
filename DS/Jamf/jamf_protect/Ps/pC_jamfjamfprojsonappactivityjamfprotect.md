#### Parser Content
```Java
{
Name = jamf-jamfpro-json-app-activity-jamfprotect
  Vendor = "Jamf"
  Product = "Jamf Protect"
  ExtractionType = json
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """"effective_user_name":""", """"host_info":""", """"event_name":""", """"AUE_""" ]
  Fields = [
    """exa_json_path=$.host_info.host_name,exa_field_name=host""",
    """exa_json_path=$..thread_uuid,exa_field_name=user_uid""",
    """exa_json_path=$.host_info.serial_number,exa_field_name=host_key""",
    """exa_json_path=$.host_info.osversion,exa_field_name=os_revision""",
    """exa_json_path=$.host_info.host_uuid,exa_field_name=connection_uid""",
    """exa_json_path=$.exec_args.args_compiled,exa_field_name=additional_info""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.return.description,exa_field_name=result""",
    """exa_json_path=$.header.event_name,exa_field_name=event_name""",
    """exa_json_path=$.header.event_id,exa_field_name=event_code""",
    """exa_json_path=$.subject.process_id,exa_field_name=process_id""",
    """exa_json_path=$.subject.effective_user_name,exa_field_name=user""",
    """exa_json_path=$.subject.effective_group_name,exa_field_name=group_name""",
    """exa_json_path=$.subject.effective_group_id,exa_field_name=group_id""",
    """exa_json_path=$.subject.effective_user_id,exa_field_name=user_id""",
    """exa_json_path=$.subject.session_id,exa_field_name=session_id""",
    """exa_json_path=$.path,exa_field_name=path""",
    """exa_json_path=$.subject.process_name,exa_regex=({process_path}({process_dir}[^"]+?)[\\\/]+({process_name}[^"\\\/,]+))""",
    """exa_json_path=$.socket_inet.ip_address,exa_field_name=src_ip""",
    """exa_json_path=$.socket_inet.port,exa_field_name=src_port""",
    """exa_json_path=$.subject.user_id,exa_field_name=user_id""",
    """exa_json_path=$.subject.process_hash,exa_field_name=process_hash"""
  ]


}
```