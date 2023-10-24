#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-session-fail-4653-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 4653 """,""" MSWinEventLog """, """Main Mode An IPsec main mode negotiation failed""" ]
  Fields = [
    """ ({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d)""",
    """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}4653)""",
    """({event_name}An IPsec main mode negotiation failed)""",
    """Local Endpoint:.*?Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Keying Module Port:\s*({src_port}\d+)""",
    """Remote Endpoint:.*?Network Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Keying Module Port:\s*({dest_port}\d+)""",
    """Authentication Method:\s*(-|({auth_method}\S.*?))\s*Role:""",
    """Failure Reason:\s*(-|({failure_reason}.+?))\s*State:"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```