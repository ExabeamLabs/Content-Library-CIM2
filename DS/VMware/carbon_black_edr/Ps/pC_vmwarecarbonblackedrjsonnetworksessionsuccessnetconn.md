#### Parser Content
```Java
{
Name = vmware-carbonblackedr-json-network-session-success-netconn
  Vendor = VMware
  Product = Carbon Black EDR
  ParserVersion = v1.0.0
  TimeFormat = epoch_sec
  ExtractionType = json
  Conditions = [ """"process_guid"""", """ingress.event.netconn""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.type,exa_field_name=operation_type"""
    """exa_json_path=$.computer_name,exa_field_name=src_host"""
    """exa_json_path=$.sensor_id,exa_field_name=sensor_id"""
    """exa_json_path=$.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.pid,exa_field_name=process_id"""
    """exa_json_path=$.process_guid,exa_field_name=process_guid"""
    """exa_json_path=$.local_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.remote_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.remote_port,exa_field_name=dest_port"""
    """exa_json_path=$.domain,exa_field_name=web_domain"""
] 


}
```