#### Parser Content
```Java
{
Name = vmware-carbonblackedr-json-network-traffic-success-edr
  ParserVersion = v1.0.0
  Product = Carbon Black EDR
  Conditions = [ """"type":"endpoint.event.netconn"""", """"process_username":"""", """"event_origin":"EDR"""" ]
  Fields = ${CarbonBlackParsersTemplates.carbonblack-edr.Fields} [
     """exa_json_path=$.parent_path,exa_regex=({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
    
  ]

carbonblack-edr = {
    Vendor = VMware
    Product = Carbon Black EDR
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Fields = [
      """"+process_cmdline"+:"+\s*({process_command_line}[^"]+?)\s*"+,""",
      """"+process_username"+:"+(({domain}[^\\,]+)\\+)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+""",
      """"+process_pid"+:({process_id}\d+)""",
      """"+device_name"+:"+([^\\"]+\\+)?({host}[^"]+)"+""",
      """"+sensor_action"+:"+({action}[^"]+)"+""",
      """"+process_path"+:"+((?i)(SYSTEM)|({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+)))"""",
      """"+action"+:"+({action}[^"]+)?"*""",
      """"+parent_cmdline"+:"+\s*({parent_process_command_line}[^"]+?)\s*",""",
      """"+parent_pid"+:({parent_process_id}\d+)""",
      """"+process_guid"+:"+({process_guid}[^"]+)?"*\,""",
      """"+parent_guid"+:"+({parent_process_guid}[^"]+)?"*\,""",
      """"+alert_id"+:"+({alert_id}[^,]"+)?\,""",
      """"+type"+:"+({operation_type}[^"]+)"+""",
      """"device_id"+:"+({device_id}[^",]+)""",
      """"device_external_ip"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"device_os"+:"+({os}[^",]+)""",
      """"device_timestamp"+:"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
      """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""",
    """exa_json_path=$.process_cmdline,exa_field_name=process_command_line"""
    """exa_json_path=$.process_username,exa_regex=(({domain}[^\\,]+)\\+)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.process_pid,exa_field_name=process_id"""
    """exa_json_path=$.device_name,exa_regex=(\w+\\+)?({host}[^."]+)"""
    """exa_json_path=$.sensor_action,exa_field_name=action"""
    """exa_json_path=$.process_path,exa_regex=((?i)(SYSTEM)|({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+)))"""
    """exa_json_path=$.action,exa_field_name=action"""
    """exa_json_path=$.parent_cmdline,exa_field_name=parent_process_command_line"""
    """exa_json_path=$.parent_pid,exa_field_name=parent_process_id"""
    """exa_json_path=$.process_guid,exa_field_name=process_guid"""
    """exa_json_path=$.parent_guid,exa_field_name=parent_process_guid"""
    """exa_json_path=$.alert_id,exa_field_name=alert_id"""
    """exa_json_path=$.type,exa_field_name=operation_type"""
    """exa_json_path=$.device_id,exa_field_name=device_id"""
    """exa_json_path=$.device_external_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.device_timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """exa_json_path=$.device_os,exa_field_name=os"""
    """exa_regex=parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
    
}
```