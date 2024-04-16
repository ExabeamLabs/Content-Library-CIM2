#### Parser Content
```Java
{
Name = cisco-securenwanalytics-json-network-session-success-serviceid
  Vendor = Cisco
  Product = Cisco Secure Network Analytics
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch"
  ExtractionType = json
  Conditions = [ """app_id":""", """protocol":""", """service_id":""", """nbar_app_id":"""  ]
  Fields = [
   """exa_json_path=$.start_time,exa_field_name=time"""
   """exa_json_path=$.service,exa_field_name=service_name"""
   """exa_json_path=$.protocol,exa_field_name=protocol"""
   """exa_json_path=$.service_id,exa_field_name=service_id"""
   """exa_json_path=$.endpoint2_port,exa_regex=({src_port}\d+)"""
   """exa_json_path=$.endpoint1_port,exa_regex=({dest_port}\d+)"""
   """exa_json_path=$.endpoint1_bytes,exa_field_name=bytes_out"""
   """exa_json_path=$.app_id,exa_field_name=app_id"""
    """exa_regex="username"+:\s*"({user}[\w\.\-]{1,40}\$?)"""
    """exa_json_path=$.endpoint2_packets,exa_field_name=bytes_in"""
    """exa_regex="endpoint1_ip_address"+:\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
    """exa_json_path=$.endpoint2_mac_address,exa_field_name=src_mac"""
    """exa_regex="endpoint1_ip_address"+:\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
    """exa_json_path=$.endpoint1_mac_address,exa_field_name=dest_mac"""
    """exa_regex="endpoint2_ip_address"+:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]


}
```