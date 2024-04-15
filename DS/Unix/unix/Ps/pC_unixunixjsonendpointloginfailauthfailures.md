#### Parser Content
```Java
{
Name = "unix-unix-json-endpoint-login-fail-authfailures"
Product = "Unix"
Conditions = [
  """"decoder.name":"sshd""""
  """Too many authentication failures for"""
  """"type":"wazuh-alerts""""
]
ParserVersion = "v1.0.0"

SSSZ"
    Fields = [
      """"data.id":"({event_code}\d+)"""",
      """"@timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """"data.dstuser":"(\(no user\)|({dest_user}[^"]+))""",
      """"data.status":"({result}[^"]+)""",
      """"location":"({log_location}[^"]+)""",
      """"data.data":"({data}[^"]+)""",
      """"path":"({log_path}[^"]+)""",
      """"data.system_name":"({host}[^"]+)""",
      """"agent.id":"({agent_id}\d+)""",
      """"manager.name":"({wazuh_manager}[^"]+)""",
      """"data.data":"({data}[^"]+)""",
      """"rule.description":"({description}[^"]+)""",
      """"decoder.name":"({decoder_name}[^"]+)"""
    
}
```