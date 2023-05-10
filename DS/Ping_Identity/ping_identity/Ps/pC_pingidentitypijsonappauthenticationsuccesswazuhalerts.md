#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-authentication-success-wazuhalerts
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  Conditions = [ """"data.type":"AUTHN_ATTEMPT"""", """"type":"wazuh-alerts"""" ]

wazuh-ping-app-template {
    Vendor = Ping Identity
    Product = Ping Identity
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
      """"data.username":"(({email_address}[^"]+?@[^"]+?\.[^"]+?)|({user}[^"]+?))""""
      """"data.ip_address":"({src_ip}[:0-9a-fA-F\.]+)\s*""""
      """"data.hostname":"({host}[^"]+)"""
      """"location":"({log_location}[^"]+)"""
      """"path":"({log_path}[^"]+)"""
      """"agent.id":"({agent_id}\d+)"""
      """"manager.name":"({wazuh_manager}[^"]+)"""
      """"rule.description":"({description}[^"]+)"""
      """"decoder.name":"({decoder_name}[^"]+)"""
      """"rule.id":"({rule_id}\d+)"""
      """"agent.name":"({agent_name}[^"]+)"""
      """"agent.id":"({agent_id}[^"]+)"""
      """"data.status":"({result}[^"]+)"""
      """({app}Ping)"""
      """"data.link2":"({app}[^"]+)"""
      """"data.type":"({additional_info}[^"]+)"""
    ]
    DupFields = [ "description->event_name" 
}
```