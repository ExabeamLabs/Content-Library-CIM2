#### Parser Content
```Java
{
Name = ossec-o-json-app-activity-success-wazuhalerts
  ParserVersion = "v1.0.0"
  Vendor = OSSEC
  Product = OSSEC
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = ["""syscheck_integrity_changed""", """wazuh-manager""" , """"type":"wazuh-alerts""""  ]
  Fields = [
    """"host":"({host}[^"]+)""",
    """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """"rule.description":"({description}[^"]+)"""
    """"path":"({log_path}[^"]+)"""
    """"cluster.name":"({cluster_name}[^"]+)""",
# cluster_node is removed
    """"location":"({log_location}[^"]+)"""
    """"rule.id":"({rule_id}[^"]+)"""
    """"decoder.name":"({decoder_name}[^"]+)"""
    """"agent.name":"({agent_name}[^"]+)"""
    """"syscheck.md5_after":"({new_hash}[^"]+)""",
    """"syscheck.md5_before":"({old_hash}[^"]+)""",
  ]


}
```