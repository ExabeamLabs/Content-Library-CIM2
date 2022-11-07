#### Parser Content
```Java
{
Name = cisco-asa-kv-app-notification-adjchg
  ParserVersion = "v1.0.0"
  Conditions = [ """%OSPF-""", """ADJCHG:""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """ADJCHG:\s*.+?({event_name}Nbr ({src_ip}[A-Fa-f:\d.]+)[^,]+)""",
    """Neighbor Down:\s*({failure_reason}.+?)\s+$""",
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