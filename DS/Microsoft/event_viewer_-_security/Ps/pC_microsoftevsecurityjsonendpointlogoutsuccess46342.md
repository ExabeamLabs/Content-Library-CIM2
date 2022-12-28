#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-success-4634-2
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """"data.id":"4634"""", """"type":"wazuh-alerts""""  , """"decoder.parent":"windows"""" ]
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
    """({event_name}An account was logged off)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}\S+)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Logon Type:""",
    """Logon Type:\s*({login_type}\d+)""",
  ]


}
```