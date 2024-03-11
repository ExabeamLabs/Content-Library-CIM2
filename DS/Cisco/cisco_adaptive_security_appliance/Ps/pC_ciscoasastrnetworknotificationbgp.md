#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-bgp
  ParserVersion = v1.0.0
  Conditions = [ """%BGP""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s(pdt|PDT):"""
    """({event_code}%BGP-[^:]+)""",
    """({protocol}BGP)""",
# neighbor_ip is removed
    """ad.message=({event_name}.*?(UP|DOWN))\s*(\(?({failure_reason}.*?)?\))?\said"""
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