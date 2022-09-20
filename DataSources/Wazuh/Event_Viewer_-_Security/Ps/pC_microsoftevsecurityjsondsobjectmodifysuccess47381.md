#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-ds-object-modify-success-4738-1
  Product = Event Viewer - Security
  Conditions = [ """"data.id":"4738"""", """"type":"wazuh-alerts"""", """"decoder.parent":"windows""""  ]
  Fields = ${WazuhParserTemplates.wazuh-windows-template.Fields} [
    """({event_name}A user account was changed)""",
    """Security ID:\s*(|({user_sid}.+?))\s+Account Name:""",
    """Account Name:\s*(|({user}.+?))\s+Account Domain:\s*(|({domain}.+?))\s+Logon ID:\s*(|({login_id}.+?))\s+Target Account:""",
    """Target\sAccount.+?Security ID:\s*({target_sid}.+?)\s""",
    """Target\sAccount.+?Account Name:\s*({dest_user}.+?)\s""",
    """Target\sAccount.+?Account Domain:\s*({dest_domain}.+?)\s""",
    """Changed Attributes:\s*(|({attribute}.+?))\s+SAM Account Name"""
  ]
  ParserVersion = "v1.0.0"

wazuh-windows-template = {
    Vendor = Wazuh
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"data.id":"({event_code}\d )"""",
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