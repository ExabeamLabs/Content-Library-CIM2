#### Parser Content
```Java
{
Name = cisco-securenwanalytics-json-network-session-success-flow_id
  Vendor = Cisco
  Product = Cisco Secure Network Analytics
  ParserVersion = "v1.0.0"
  TimeFormat =  "epoch"
  Conditions = [ """app_id":""", """inbound_packets":""", """flow_id":""", """firewall_action":""" ]
  ExtractionType = json
  Fields = [
      """exa_json_path=$.last_time,exa_field_name=time""" 
      """exa_json_path=$.service,exa_field_name=service_name"""
      """exa_json_path=$.protocol,exa_field_name=protocol"""
      """exa_json_path=$.service_id,exa_field_name=service_id"""
      """exa_json_path=$.client_ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.server_ip_address,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_json_path=$.inbound_bytes,exa_field_name=bytes_in"""
      """exa_json_path=$.inbound_packets,exa_field_name=packets_in"""
      """exa_json_path=$.outbound_bytes,exa_field_name=bytes_out"""
      """exa_json_path=$.outbound_packets,exa_field_name=packets_out"""
      """exa_json_path=$.ttl,exa_field_name=response_ttl"""
      """exa_json_path=$.firewall_action,exa_field_name=action"""
      """exa_json_path=$.total_bytes,exa_regex=(null|({bytes}\d+))"""
  ]


}
```