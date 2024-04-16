#### Parser Content
```Java
{
Name = cisco-asa-cef-network-notification-neighbor
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","epoch"]
  Conditions = [ """%LDP-5-NBRCHG:""", """|LDP:NBRCHG|Neighbor|""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """({event_code}%[\s\w+-]+):""",
        """({protocol}LDP)"""
# neighbor_ip is removed
        """ad.message=({event_name}.*?(UP|DOWN))\s*(\(?({failure_reason}.*?)?\))?\said""",
        """\Wrt=({time}\d{13})"""
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