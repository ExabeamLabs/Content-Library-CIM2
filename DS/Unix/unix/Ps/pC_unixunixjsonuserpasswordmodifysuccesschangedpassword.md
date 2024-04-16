#### Parser Content
```Java
{
Name = unix-unix-json-user-password-modify-success-changedpassword
  Product = Unix
  Vendor = Unix
  ExtractionType = json
  Conditions = [ """"type":"wazuh-alerts"""", """"rule.description":"PAM: User changed password."""" ]
  ParserVersion = "v1.0.0"
  
wazuh-common-fields {
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """exa_json_path=$.@timestamp,exa_field_name=time"""
      """exa_json_path=$.location,exa_field_name=log_location"""
      """exa_json_path=$.path,exa_field_name=log_path"""
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id"""
      """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager"""
      """exa_json_path=$.['rule.description'],exa_field_name=description""",
      """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
      """exa_json_path=$.['rule.id'],exa_field_name=rule_id"""
      """exa_json_path=$.['agent.name'],exa_field_name=agent_name""",
      """exa_json_path=$.['predecoder.hostname'],exa_field_name=host""",
      """exa_json_path=$.['data.dstuser'],exa_field_name=dest_user""",
      """exa_regex="agent\.labels\.network\.ipv4\.primary":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]
    DupFields=["host->dest_host", "description->event_name"
}
```