#### Parser Content
```Java
{
Name = wazuh-w-json-endpoint-activity-success-wazuhalerts-1
  ParserVersion = "v1.0.0"
  Conditions = [ """"decoder.parent":"windows"""" , """"type":"wazuh-alerts""""  , """"data.id":""""]

dl-wazuh-windows-template = {
    Vendor = Wazuh
    Product = Wazuh
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"data.id":"({event_code}\d+)""""
      """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
      """"data.dstuser":"(\(no user\)|({dest_user}[^"]+))"""
      """"data.status":"({result}[^"]+)"""
      """"location":"({log_location}[^"]+)"""
      """"data.data":"({data}[^"]+)"""
      """"path":"({log_path}[^"]+)"""
      """"data.system_name":"({host}[^"]+)"""
      """"agent.id":"({agent_id}\d+)"""
      """"manager.name":"({wazuh_manager}[^"]+)"""
      """"rule.description":"({description}[^"]+)"""
      """"decoder.name":"({decoder_name}[^"]+)"""
    
}
```