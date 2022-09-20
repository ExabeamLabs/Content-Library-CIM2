#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-dual
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  Conditions = [ """%DUAL-""", """NBRCHANGE:""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """({event_code}%DUAL-[^:]+)""",
    """Neighbor ({src_ip}[A-Fa-f:\d.]+)""",
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```