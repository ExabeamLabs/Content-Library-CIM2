#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-request-success-4656
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = v1.0.0
  Conditions = [ """"data.id":"4656"""", """"type":"wazuh-alerts""""  , """"decoder.parent":"windows""""  ]
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
    """({event_name}A handle to an object was requested)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:\s*({object_class}.+?)\s*Object Name:""",
    """Object Name:\s*({object}\S.*?)\s*Handle ID:""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """Process Name:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s*Access Request Information:""",
    """Transaction ID:\s*({transaction_id}[^\s]+)\s*Accesses:""",
    """Accesses:\s*({access}\S.*?)\s*Access Reasons:""",
    """Access Reasons:\s*(-|({access}\S.*?))\s*Access Mask:""",
    """Privileges Used for Access Check:\s*(-|({privileges}.*?))\s*Restricted SID Count:""",
    """({operation_type}requested)""",
    """Handle ID:\s*({object_id}.+?)\s""",
  ]


}
```