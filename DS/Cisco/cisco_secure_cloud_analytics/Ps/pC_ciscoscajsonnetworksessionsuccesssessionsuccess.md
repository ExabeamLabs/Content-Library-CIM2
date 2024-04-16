#### Parser Content
```Java
{
Name = cisco-sca-json-network-session-success-sessionsuccess
  Vendor = Cisco
  Product = Cisco Secure Cloud Analytics
  TimeFormat = "yyyy-MM-dd HH:mm:ss" 
  flow_start_timeFormat = ["yyyy-MM-dd HH:mm:ss"]
  flow_end_timeFormat = ["yyyy-MM-dd HH:mm:ss"]
  ExtractionType = json
  Conditions = [ """"connected_ipv6":""", """"netid":""", """"octets_in":""", """"profile_tag":""" ] 
  Fields = [
      """exa_json_path=$.start_timestamp_utc,exa_field_name=flow_start_time"""
      """exa_json_path=$.end_timestamp_utc,exa_field_name=flow_end_time"""
      """exa_json_path=$.port,exa_field_name=src_port"""
      """exa_json_path=$.connected_port,exa_field_name=dest_port"""
      """exa_json_path=$.protocol,exa_field_name=protocol"""
      """exa_json_path=$.octets_in,exa_field_name=bytes_in"""
      """exa_json_path=$.octets_out,exa_field_name=bytes_out"""
      """exa_json_path=$.packets_in,exa_field_name=packets_in"""
      """exa_json_path=$.packets_out,exa_field_name=packets_out"""
      """exa_json_path=$.first_direction,exa_field_name=direction"""
      """exa_json_path=$.profile_tag,exa_field_name=additional_info"""
      """exa_json_path=$.flags,exa_field_name=tcp_flags"""
      """exa_json_path=$.device_id,exa_field_name=device_id"""
      """exa_json_path=$.ipv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.connected_ipv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_regex=({bytes_unit}(?i)octets)"""
  ]
  DupFields = [ "flow_start_time->time" ]
  ParserVersion = "v1.0.0"


}
```