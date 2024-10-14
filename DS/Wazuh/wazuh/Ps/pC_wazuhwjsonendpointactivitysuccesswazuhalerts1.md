#### Parser Content
```Java
{
Name = wazuh-w-json-endpoint-activity-success-wazuhalerts-1
  ParserVersion = "v1.0.0"
  Conditions = [ """"decoder.parent":"windows"""" , """"type":"wazuh-alerts""""  , """"data.id":""""]

dl-wazuh-windows-template = {
    Vendor = Wazuh
    Product = Wazuh
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """exa_regex="data.id":"({event_code}\d+)"""",
      """exa_json_path=$.@timestamp,exa_field_name=time""",
      """exa_json_path=$.['data.dstuser'],exa_regex=^(\(no user\)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """exa_json_path=$.['data.status'],exa_field_name=result""",
      """exa_json_path=$.location,exa_field_name=log_location"""
      """exa_json_path=$.['data.data'],exa_field_name=data""",
      """exa_json_path=$.path,exa_field_name=log_path"""
      """exa_json_path=$.['data.system_name'],exa_field_name=host"""
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id"""
      """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager"""
      """exa_json_path=$.['rule.description'],exa_field_name=description""",
      """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
    
}
```