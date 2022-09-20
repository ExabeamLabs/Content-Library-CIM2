#### Parser Content
```Java
{
Name = airlock-waf-str-app-notification-webrequests
  Vendor = Airlock
  Product = Web Application Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ Web-Requests:""", """rid:""", """sid:""" ]
  Fields = [
    """({host}[\w\-.]+)\s+Web-Requests:""",
# rid is removed
    """sid:({user_sid}[^\s]+)""",
    """ip:({src_ip}[A-Fa-f:\d.]+)""",
# m_value is removed
  ]


}
```