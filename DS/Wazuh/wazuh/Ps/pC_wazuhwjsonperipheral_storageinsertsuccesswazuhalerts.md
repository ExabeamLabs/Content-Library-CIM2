#### Parser Content
```Java
{
Name = wazuh-w-json-peripheral_storage-insert-success-wazuhalerts
  ParserVersion = "v1.0.0"
  Product = Wazuh
  Vendor = Wazuh
  Conditions = [ """"rule.description":"Attached USB Storage"""", """"type":"wazuh-alerts"""" ]
  Fields = ${DLWazuhParserTemplates.wazuh-catch-all-template.Fields} [
    """exa_regex=({additional_info}idVendor=\d+, idProduct=\d+)"""
    """exa_json_path=$.['agent.labels.agent_hostname'],exa_regex=({src_host}[\w\-.]+)""" 
 ]

wazuh-catch-all-template {
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields = [
      """exa_json_path=$.@timestamp,exa_field_name=time""",
      """exa_json_path=$.['data.dstuser'],exa_regex=^(\(no user\)|({dest_user}[\w\.\-]{1,40}\$?))""",
      """exa_json_path=$.location,exa_field_name=log_location"""
      """exa_json_path=$.path,exa_field_name=log_path"""
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id"""
      """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager"""
      """exa_json_path=$.['rule.description'],exa_field_name=description""",
      """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
      """exa_json_path=$.['rule.id'],exa_field_name=rule_id"""
      """exa_json_path=$.['agent.name'],exa_field_name=agent_name""",
      """exa_json_path=$.['data.srcip'],exa_regex="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.['data.status'],exa_field_name=result""",
      """exa_json_path=$.['data.data'],exa_field_name=data""",
      """exa_json_path=$.['predecoder.hostname'],exa_field_name=host""",
      """exa_json_path=$.['data.system_name'],exa_field_name=host"""
      """exa_json_path=$.['agent.labels.os.name'],exa_field_name=os"""
    ]
    DupFields = [ "dest_user->user" 
}
```