#### Parser Content
```Java
{
Name = "cisco-fp-json-network-session-connection-fw"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"originator_type":"FTD"""",
  """"firewall_rule_list":"""
]
ExtractionType = json
Fields = [
      """exa_json_path=$.first_packet_second,exa_field_name=time"""
      """exa_json_path=$.device_uuid,exa_field_name=device_id"""
      """exa_json_path=$.context,exa_field_name=additional_info"""
      """exa_json_path=$.ingress_interface,exa_field_name=dest_interface"""
      """exa_json_path=$.ingress_zone,exa_field_name=ingress_zone"""
      """exa_json_path=$.egress_interface,exa_field_name=src_interface"""
      """exa_json_path=$.egress_zone,exa_field_name=egress_zone"""
      """exa_json_path=$.initiator_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.initiator_port,exa_field_name=src_port"""
      """exa_json_path=$.initiator_packets,exa_field_name=initiator_packets"""
      """exa_json_path=$.initiator_bytes,exa_field_name=bytes_out"""
      """exa_json_path=$.responder_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_json_path=$.responder_port,exa_field_name=dest_port"""
      """exa_json_path=$.responder_packets,exa_field_name=responder_packets"""
      """exa_json_path=$.responder_bytes,exa_field_name=bytes_in"""
      """exa_json_path=$.protocol,exa_field_name=protocol"""
      """exa_json_path=$.tcp_flags,exa_field_name=tcp_flags"""
      """exa_json_path=$.dns_response_type,exa_field_name=dns_response_code"""
      """exa_json_path=$.client_application,exa_field_name=network_app"""
      """exa_json_path=$.firewall_policy,exa_field_name=policy_name"""
      """exa_json_path=$.firewall_rule_list,exa_field_name=rule"""
      """exa_json_path=$.nap_policy,exa_field_name=nap_policy"""
      """exa_json_path=$.ac_rule_action,exa_field_name=result"""
      """exa_json_path=$.ssl_actual_action,exa_field_name=action"""
      """exa_json_path=$.url,exa_field_name=url"""
      """exa_json_path=$.url_category,exa_field_name=category"""
      """exa_json_path=$.url_reputation,exa_field_name=reputation"""
]
ParserVersion = "v1.0.0"


}
```