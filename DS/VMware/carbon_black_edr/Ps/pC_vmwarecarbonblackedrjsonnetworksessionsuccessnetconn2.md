#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-json-network-session-success-netconn-2"
  Vendor = "VMware"
  ParserVersion = "v1.0.0"
  Product = "Carbon Black EDR"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  ExtractionType = json
  Conditions = [
    """netconn"""
    """carbonblack"""
    """sensor_action"""
  ]
  Fields = [
    """exa_regex=({time}\d+-\d+-\d+ \d+:\d+:\d+.\d\d\d)"""
    """exa_json_path=$.process_cmdline,exa_field_name=process_command_line"""
    """exa_json_path=$.process_username,exa_regex=(NT AUTHORITY\\+|(({domain}[^\\,]+)\\+))?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.process_pid,exa_field_name=process_id"""
    """exa_json_path=$.device_name,exa_regex=(\w+\\+)?({host}[^.\"]+)"""
    """exa_json_path=$.sensor_action,exa_field_name=result"""
    """exa_json_path=$.process_path,exa_regex=({process_path}({process_dir}[^\"]+(\\|\/)+)?({process_name}[^\"]+))"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.parent_cmdline,exa_field_name=parent_process_command_line"""
    """exa_json_path=$.parent_pid,exa_field_name=parent_process_id"""
    """exa_json_path=$.process_guid,exa_field_name=process_guid"""
    """exa_json_path=$.parent_guid,exa_field_name=parent_process_guid"""
    """exa_json_path=$.alert_id,exa_field_name=alert_id"""
    """exa_json_path=$.local_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.remote_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.remote_port,exa_field_name=dest_port"""
    """exa_json_path=$.local_port,exa_field_name=src_port"""
    """exa_json_path=$.type,exa_field_name=operation_type"""
    """exa_json_path=$.netconn_protocol,exa_regex=(PROTO_)?({protocol}[^\"]+)"""
  ]
  DupFields = [
    "operation_type->event_name"
  ]


}
```