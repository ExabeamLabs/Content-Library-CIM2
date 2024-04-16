#### Parser Content
```Java
{
Name = "unix-unix-json-endpoint-login-fail-authfailures"
Product = "Unix"
ExtractionType = json
Conditions = [
  """"decoder.name":"sshd""""
  """Too many authentication failures for"""
  """"type":"wazuh-alerts""""
]
ParserVersion = "v1.0.0"

SSSZ"
    Fields = [
      """exa_json_path=$.['data.id'],exa_field_name=event_code""",
      """exa_json_path=$.@timestamp,exa_field_name=time""",
      """exa_json_path=$.['data.dstuser'],exa_field_name=dest_user,exa_match_expr=!Contains($.['data.dstuser'],"(no user)")""",
      """exa_json_path=$.['data.status'],exa_field_name=result""",
      """exa_json_path=$.location,exa_field_name=log_location""",
      """exa_json_path=$.['data.data'],exa_field_name=data""",
      """exa_json_path=$.path,exa_field_name=log_path""",
      """exa_json_path=$.['data.system_name'],exa_regex=^({host}[\w\-.]+)$""",
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id""",
      """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager""",
      """exa_json_path=$.['rule.description'],exa_field_name=description""",
      """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
    
}
```