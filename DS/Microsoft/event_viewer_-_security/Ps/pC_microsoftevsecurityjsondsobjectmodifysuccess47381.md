#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-ds-object-modify-success-4738-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  Conditions = [ """"data.id":"4738"""", """"type":"wazuh-alerts"""", """"decoder.parent":"windows""""  ]
  Fields = ${WazuhParserTemplates.wazuh-windows-template.Fields} [
    """({event_name}A user account was changed)""",
    """Security ID:\s*(|({user_sid}.+?))\s+Account Name:""",
    """Account Name:\s*(|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:\s*(|({domain}.+?))\s+Logon ID:\s*(|({login_id}.+?))\s+Target Account:""",
    """Target\sAccount.+?Security ID:\s*({target_sid}.+?)\s""",
    """Target\sAccount.+?Account Name:\s*({dest_user}.+?)\s""",
    """Target\sAccount.+?Account Domain:\s*({dest_domain}.+?)\s""",
    """Changed Attributes:\s*(|({attribute}.+?))\s+SAM Account Name"""
  ]
  ParserVersion = "v1.0.0"

wazuh-windows-template = {
    Vendor = Wazuh
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
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