#### Parser Content
```Java
{
Name = wazuh-w-json-alert-trigger-wazuhalerts
  ParserVersion = "v1.0.0"  
  Vendor = Wazuh
  Product = Wazuh
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"System Audit:""", """"ossec"""", """"type":"wazuh-alerts"""" ]
  Fields = [
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.@timestamp,exa_field_name=time"""
    """exa_json_path=$.['rule.description'],exa_field_name=description""",
    """exa_json_path=$.path,exa_field_name=log_path"""
    """exa_json_path=$.['cluster.name'],exa_field_name=cluster_name""",
# cluster_node is removed
    """exa_regex=data.file":"({file_path}({file_dir}[^,]*?)[\\\/]*({file_name}[^,\\\/]+?))"""",
    """exa_json_path=$.location,exa_field_name=log_location"""
    """exa_json_path=$.['data.title'],exa_field_name=data"""
    """exa_json_path=$.['rule.id'],exa_field_name=rule_id"""
    """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
    """exa_json_path=$.['agent.name'],exa_field_name=agent_name"""
# reference is removed
    """exa_json_path=$.type,exa_field_name=alert_type"""
    """exa_json_path=$.['rule.level'],exa_field_name=alert_severity"""
  ]
  DupFields = [ "data->event_name", "agent_name -> alert_source" , "data -> alert_name"]


}
```