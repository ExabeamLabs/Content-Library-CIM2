#### Parser Content
```Java
{
Name = wazuh-w-json-alert-trigger-wazuhalerts
  ParserVersion = "v1.0.0"  
  Vendor = Wazuh
  Product = Wazuh
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"System Audit:""", """"ossec"""", """"type":"wazuh-alerts"""" ]
  Fields = [
    """"host":"({host}[^"]+)""",
    """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """"rule.description":"({description}[^"]+)"""
    """"path":"({log_path}[^"]+)"""
    """"cluster.name":"({cluster_name}[^"]+)""",
# cluster_node is removed
    """data.file":"({file_path}({file_dir}[^,]*?)[\\\/]*({file_name}[^,\\\/]+?))"""",
    """"location":"({log_location}[^"]+)"""
    """"data.title":"({data}[^"]+)"""
    """"rule.id":"({rule_id}[^"]+)"""
    """"decoder.name":"({decoder_name}[^"]+)"""
    """"agent.name":"({agent_name}[^"]+)"""
# reference is removed
    """"type":"({alert_type}[^"]+)""""
    """"rule.level":({alert_severity}\d+),"""
  ]
  DupFields = [ "data->event_name", "agent_name -> alert_source" , "event_name -> alert_name"]


}
```