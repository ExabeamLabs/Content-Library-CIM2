#### Parser Content
```Java
{
Name = unix-unix-json-user-password-modify-success-changedpassword
  Product = Unix
  Vendor = Unix
  Conditions = [ """"type":"wazuh-alerts"""", """"rule.description":"PAM: User changed password."""" ]
  Fields = ${WazuhParserTemplates.wazuh-common-fields.Fields} [
    """"predecoder.hostname":"({host}[^"]+)""",
    """"data.dstuser":"({dest_user}[^"]+)""",
    """"agent\.labels\.network\.ipv4\.primary":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"
  DupFields=["host->dest_host", "description->event_name"]

wazuh-common-fields {
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
      """"location":"({log_location}[^"]+)"""
      """"path":"({log_path}[^"]+)"""
      """"agent.id":"({agent_id}\d+)"""
      """"manager.name":"({wazuh_manager}[^"]+)"""
      """"rule.description":"({description}[^"]+)"""
      """"decoder.name":"({decoder_name}[^"]+)"""
      """"rule.id":"({rule_id}\d+)"""
      """"agent.name":"({agent_name}[^"]+)"""
      """"agent.id":"({agent_id}[^"]+)"""
    
}
```