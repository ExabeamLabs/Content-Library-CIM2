#### Parser Content
```Java
{
Name = infoblox-bddi-json-dns-query-success-response
    Vendor = Infoblox
    Product = BloxOne DDI
    ExtractionType = json
    TimeFormat = "epoch"
    Conditions = [ """"query_type"""", """"response"""", """"qname"""", """"qclass"""" ]
    Fields = [
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_json_path=$.qip,exa_field_name=src_ip"""
      """exa_json_path=$.qname,exa_field_name=dns_query"""
      """exa_json_path=$.extra.query_type,exa_field_name=dns_query_type"""
      """exa_json_path=$.extra.policy_action,exa_field_name=action"""
      """exa_json_path=$.extra.all_tags,exa_field_name=tags"""
      """exa_json_path=$.username,exa_field_name=user"""
      """exa_json_path=$.extra.user_name,exa_field_name=user"""
      """exa_json_path=$.extra.response,exa_field_name=dns_response_code"""
      """exa_json_path=$.extra.device_name,exa_field_name=host"""
      """exa_json_path=$.extra.os_version,exa_field_name=os"""
      """exa_json_path=$.extra.device_ip,exa_field_name=device_ip"""
      """exa_json_path=$.qport,exa_field_name=src_port"""
      """exa_json_path=$.protocol,exa_field_name=protocol"""
      """exa_json_path=$.opcode,exa_field_name=opcode"""
      """exa_json_path=$.extra.threat_indicator,exa_field_name=ioc"""

    ]
    ParserVersion = "v1.0.0"
  

}
```