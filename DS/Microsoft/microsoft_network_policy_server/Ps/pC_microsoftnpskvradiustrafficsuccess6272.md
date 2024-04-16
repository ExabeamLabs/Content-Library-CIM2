#### Parser Content
```Java
{
Name = microsoft-nps-kv-radius-traffic-success-6272
  Vendor = Microsoft
  Product = Microsoft Network Policy Server
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=6272""", """Message=Network Policy Server granted access to a user""" ]
  Fields = [
    """({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""",
    """ComputerName =({host}[\w\-.]+)""",
    """EventCode=({event_code}\d+)""",
    """User:.+?Account Name:\s+(\w+(\\)+)?(?:-|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
    """User:.+?Account Domain:\s+(?:-|({domain}.+?))\s+Fully""",
    """NAS Identifier:\s+(?:-|({location}[\w\-.]+))""",
    """Calling Station Identifier:\s+(?:-|({src_mac}.+?))\s+NAS:""",
    """Authentication Server:\s+(?:-|({auth_server}.+?))\s+Authentication Type:""",
    """User:.+?Fully Qualified Account Name:\s+(?:-|({user_type}.+?))(\/[^/\s]+)?\s+Client Machine:""",
    """NAS IPv4 Address:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """NAS IPv6 Address:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """EAP Type:\s+(?:-|({auth_type}.+?))\s+Account Session Identifier:""",
    """Result:\s+(?:-|({access_type}.+?))\s+Session Identifier:"""
  ]
  ParserVersion = "v1.0.0"


}
```