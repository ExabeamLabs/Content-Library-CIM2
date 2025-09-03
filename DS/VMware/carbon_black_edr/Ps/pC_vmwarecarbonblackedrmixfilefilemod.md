#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-mix-file-filemod"
  ParserVersion = "v1.0.0"
  Conditions = [ """filemod""" , """carbonblack""" , """sensor_action""" ]

carbonblack-endpoint = { 
    Vendor = VMware
    Product = Carbon Black EDR
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    ExtractionType = json
    Fields = [
    """({time}\d+-\d+-\d+ \d+:\d+:\d+.\d\d\d)""",
    """"+process_cmdline"+:"+({process_command_line}[^"]+)"+""",
    """"+process_username"+:"+(({domain}[^\\,]+)\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+""",
    """"+process_pid"+:({process_id}\d+)""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+sensor_action"+:"+({result}[^"]+)"+""",
    """"+process_path"+:"+({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))"""",
    """"+action"+:"+({action}[^"]+)?"*""",
    """"+parent_cmdline"+:"+({parent_process_command_line}[^,]+"+)?"\,""",
    """"+parent_pid"+:({parent_process_id}\d+)""",
    """"+process_guid"+:"+({process_guid}[^"]+)?"*\,""",
    """"+parent_guid"+:"+({parent_process_guid}[^"]+)?"*\,""",
    """"+alert_id"+:"+({alert_id}[^,]"+)?\,""",
    """"+type"+:"+({operation_type}[^"]+)"+"""
    """exa_regex=({time}\d+-\d+-\d+ \d+:\d+:\d+.\d\d\d)"""
    """exa_json_path=$.process_pid,exa_field_name=process_id"""
    """exa_json_path=$.process_cmdline,exa_field_name=process_command_line"""
    """exa_json_path=$.process_username,exa_regex=(({domain}[^\\,]+)\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.device_name,exa_regex=^(\w+\\+)?({host}[^."]+)$"""
    """exa_json_path=$.sensor_action,exa_field_name=result"""
    """exa_json_path=$.process_path,exa_regex=({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.parent_cmdline,exa_regex=({parent_process_command_line}[^,]+"+)?"\,"""
    """exa_json_path=$.parent_pid,exa_field_name=parent_process_id"""
    """exa_json_path=$.process_guid,exa_field_name=process_guid"""
    """exa_json_path=$.parent_guid,exa_field_name=parent_process_guid"""
    """exa_json_path=$.alert_id,exa_field_name=alert_id"""
    """exa_json_path=$.type,exa_field_name=operation_type"""
   
}
```