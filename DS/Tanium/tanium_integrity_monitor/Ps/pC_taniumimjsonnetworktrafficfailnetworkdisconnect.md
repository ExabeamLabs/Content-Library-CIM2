#### Parser Content
```Java
{
Name = tanium-im-json-network-traffic-fail-networkdisconnect
  Conditions = [ """"event":"network_disconnect"""",""""remote_ip":"""",""""tanium_computer_id":"""" ]
  Fields = ${TaniumParserTemplates.tanium-operations-1.Fields}[
    """"local_port":({src_port}\d+)""",
	""""remote_port":({dest_port}\d+)""",
	""""local_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
	""""remote_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  ]
  ParserVersion = "v1.0.0"

tanium-operations-1 = {
  ExtractionType = json
  Vendor = Tanium
  Product = Tanium Integrity Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.hostname,exa_field_name=host"""
    """exa_json_path=$.fields.['login__user_name'],exa_field_name=user"""
    """exa_json_path=$.fields.['process__login__user_name'],exa_field_name=user"""
    """exa_json_path=$.event,exa_field_name=event_name"""
    """exa_json_path=$.fields.file__md5,exa_field_name=hash_md5"""
    """exa_json_path=$.fields.parent_pid,exa_field_name=process_id"""
    """exa_json_path=$.fields.command_line,exa_field_name=process_command_line"""
    """exa_json_path=$.fields.['parent__command_line'],exa_field_name=parent_process_command_line"""
    """exa_json_path=$.fields.parent_pid,exa_field_name=parent_process_id"""
  
}
```