#### Parser Content
```Java
{
Name = microsoft-adfs-kv-http-request-audit
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Active Directory Federation Service
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """An HTTP request was received.""", """Query string:""", """Request Details:""", """ audit 510 """ ]
  Fields = [
    """Date And Time:\s*({time}\d+-\d+-\d+\s\d+:\d+:\d+)""",
    """Client IP:\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """Local IP:\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
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