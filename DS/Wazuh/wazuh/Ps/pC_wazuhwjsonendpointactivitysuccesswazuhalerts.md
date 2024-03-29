#### Parser Content
```Java
{
Name = wazuh-w-json-endpoint-activity-success-wazuhalerts
  ParserVersion = "v1.0.0"
  Product = Wazuh
  Vendor = Wazuh
  Conditions = [ """"type":"wazuh-alerts"""" ]

wazuh-catch-all-template {
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
      """"data.dstuser":"(\(no user\)|({dest_user}[^"]+))"""
      """"location":"({log_location}[^"]+)"""
      """"path":"({log_path}[^"]+)"""
      """"agent.id":"({agent_id}\d+)"""
      """"manager.name":"({wazuh_manager}[^"]+)"""
      """"rule.description":"({description}[^"]+)"""
      """"decoder.name":"({decoder_name}[^"]+)"""
      """"rule.id":"({rule_id}\d+)"""
      """"agent.name":"({agent_name}[^"]+)"""
      """"agent.id":"({agent_id}[^"]+)"""
      """"data.srcip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """"data.status":"({result}[^"]+)"""
      """"data.data":"({data}[^"]+)"""
      """"predecoder.hostname":"({host}[^"]+)"""
      """"data.system_name":"({host}[^"]+)"""
      """"agent.labels.os.name":"({os}[^"]+)"""
    ]
    DupFields = [ "dest_user->user" 
}
```