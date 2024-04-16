#### Parser Content
```Java
{
Name = microsoft-adfs-kv-http-request-audit
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """An HTTP request was received.""", """Query string:""", """Request Details:""", """ audit 510 """ ]
  Fields = [
    """Date And Time:\s*({time}\d+-\d+-\d+\s\d+:\d+:\d+)""",
    """Client IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Local IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Local Port:\s*({src_port}\d+)""",
    """HTTP Method:\s*({method}[^\s]+)""",
    """Content Length:\s*({bytes}\d+)""",
    """Url Absolute Path:\s*(-|({uri_path}.+?))\s*Query string:""",
    """Query string:\s*(-|({query}.+?))\s+Local Port:""",
    """User Agent:\s*(-|({user_agent}.+?))\s+Content Length:""",
    """({event_name}An HTTP request was received)""",
  ]


}
```