#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-authentication-success-wazuhalerts
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  Conditions = [ """"data.type":"AUTHN_ATTEMPT"""", """"type":"wazuh-alerts"""" ]

wazuh-ping-app-template {
    Vendor = Ping Identity
    ExtractionType = json
    Product = Ping Identity
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """exa_json_path=$.@timestamp,exa_field_name=time"""
      """exa_json_path=$.['data.username'],exa_regex=(({email_address}[^"]+?@[^"]+?\.[^"]+?)|({user}[\w\.\-]{1,40}\$?))"""
      """exa_json_path=$.['data.ip_address'],exa_regex=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*"""
      """exa_json_path=$.['data.hostname'],exa_field_name=host"""
      """exa_json_path=$.location,exa_field_name=log_location"""
      """exa_json_path=$.path,exa_field_name=log_path"""
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id"""
      """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager"""
      """exa_json_path=$.['rule.description'],exa_field_name=description"""
      """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
      """exa_json_path=$.['rule.id'],exa_field_name=rule_id"""
      """exa_json_path=$.['agent.name'],exa_field_name=agent_name"""
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id"""
      """exa_json_path=$.['data.status'],exa_field_name=result"""
      """exa_json_path=$.['data.link2'],exa_field_name=app"""
      """exa_json_path=$.['data.type'],exa_field_name=additional_info"""
      """exa_regex=({app}Ping)"""
    ]
    DupFields = [ "description->event_name" 
}
```