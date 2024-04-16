#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-bgp
  ParserVersion = v1.0.0
  Conditions = [ """%BGP""" ]
  Fields = ${CiscoParsersTemplates.cisco-system-info.Fields} [
    """\W({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d{1,3})""",
    """(({time}\w+ \d+ \d+:\d+:\d+)\s)?({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s(pdt|PDT):""",
    """({event_code}%BGP-[^:]+)""",
    """({protocol}BGP)""",
# neighbor_ip is removed
    """ad.message=({event_name}.*?(UP|DOWN))\s*(\(?({failure_reason}.*?)?\))?\said"""
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec","epoch", "MMM dd HH:mm:ss"]
  Fields = [
    """\s({time}\w+ \d+ \d+:\d+:\d+)"""
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
     """\Wrt=({time}\d{13})""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```