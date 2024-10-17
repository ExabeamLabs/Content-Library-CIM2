#### Parser Content
```Java
{
Name = cisco-ucs-str-network-notification-success-ucsm
  Vendor = Cisco
  Product = Cisco UCS
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """%UCSM-6-EVENT""", """[FSM:""" ]
  Fields = [
    """>({time}\w{3}\s+\d{2}\s+\d{2}\:\d{2}\:\d{2})\s+({src_host}[^\s]+)\s""", 
    """:\s({alert_name}%UCSM-6[^:]+):\s""", 
    """\[({action}FSM\:[^\]]+)\]:\s+({additional_info}[^,]+)"""
  ]


}
```