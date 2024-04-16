#### Parser Content
```Java
{
Name = tanium-im-json-network-traffic-success-networkaccept
  Conditions = [ """"event":"network_accept"""",""""remote_ip"""",""""tanium_computer_id":"""" ]
  Fields = ${TaniumParserTemplates.tanium-operations-1.Fields}[
    """exa_json_path=$.fields.remote_ip,exa_field_name=dest_ip"""
    """exa_json_path=$.fields.local_ip,exa_field_name=src_ip"""
    """exa_json_path=$.fields.local_port,exa_field_name=src_port"""
    """exa_json_path=$.fields.remote_port,exa_field_name=dest_port"""
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