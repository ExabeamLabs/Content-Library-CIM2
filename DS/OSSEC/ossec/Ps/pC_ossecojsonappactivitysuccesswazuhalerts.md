#### Parser Content
```Java
{
Name = ossec-o-json-app-activity-success-wazuhalerts
  ParserVersion = "v1.0.0"
  Vendor = OSSEC
  Product = OSSEC
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""syscheck_integrity_changed""", """wazuh-manager""" , """"type":"wazuh-alerts""""  ]
  Fields = [
    """exa_json_path=$.host,exa_field_name=host"""
    """exa_json_path=$.@timestamp,exa_field_name=time"""
    """exa_json_path=$.['rule.description'],exa_field_name=description"""
    """exa_json_path=$.path,exa_field_name=log_path"""
    """exa_json_path=$.['cluster.name'],exa_field_name=cluster_name"""
    # cluster_node is removed
    """exa_json_path=$.location,exa_field_name=log_location"""
    """exa_json_path=$.['rule.id'],exa_field_name=rule_id"""
    """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
    """exa_json_path=$.['agent.name'],exa_field_name=agent_name"""
    """exa_json_path=$.['syscheck.md5_after'],exa_field_name=new_hash"""
    """exa_json_path=$.['syscheck.md5_before'],exa_field_name=old_hash"""
  ]


}
```