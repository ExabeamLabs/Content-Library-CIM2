#### Parser Content
```Java
{
Name = cisco-wlc-str-network-notification-success-apf
  Vendor = Cisco
  Product = Cisco WLC
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """%APF-4-""", """: *spamApTask""" ]
  Fields = [
    """>({time}\w{3}\s+\d{2}\s+\d{2}\:\d{2}\:\d{2})\s+({src_host}[^\s]+)\s+({host}[^:]+):\s+\*({action}.*?):"""
    """%APF-({priority}\d+)-({event_name}[^:]+):\s\w+\.c:({event_code}\d+)""",
    """({additional_info}Could not find the mobile ({src_mac}[a-fA-F\d:.]+) in internal database)"""
  ]


}
```