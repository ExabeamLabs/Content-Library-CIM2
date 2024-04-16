#### Parser Content
```Java
{
Name = "cisco-fp-json-alert-trigger-success-intrusion"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"originator_type":"FTD"""",
  """"intrusion_rule_message":"""
]
ExtractionType = json
Fields = [
      """exa_json_path=$.event_second,exa_field_name=time"""
      """exa_json_path=$.severity,exa_field_name=alert_severity"""
      """exa_json_path=$.application_id,exa_field_name=app_id"""
      """exa_json_path=$.context,exa_field_name=additional_info"""
      """exa_json_path=$.device,exa_field_name=dest_host"""
      """exa_json_path=$.device_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_json_path=$.device_uuid,exa_field_name=device_id"""
      """exa_json_path=$.egress_interface,exa_field_name=src_interface"""
      """exa_json_path=$.egress_zone,exa_field_name=egress_zone"""
      """exa_json_path=$.firewall_policy,exa_field_name=policy_name"""
      """exa_json_path=$.firewall_rule,exa_field_name=rule"""
      """exa_json_path=$.ingress_interface,exa_field_name=src_interface"""
      """exa_json_path=$.ingress_zone,exa_field_name=ingress_zone"""
      """exa_json_path=$.initiator_country_code,exa_field_name=src_country"""
      """exa_json_path=$.initiator_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.initiator_port,exa_field_name=src_port"""
      """exa_json_path=$.intrusion_policy,exa_field_name=policy_name"""
      """exa_json_path=$.protocol,exa_field_name=protocol"""
      """exa_json_path=$.responder_country_code,exa_field_name=dest_country"""
      """exa_json_path=$.responder_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_json_path=$.responder_port,exa_field_name=dest_port"""
      """exa_json_path=$.user_full_name,exa_field_name=full_name"""
      """exa_json_path=$.username,exa_field_name=user"""
]
ParserVersion = "v1.0.0"


}
```