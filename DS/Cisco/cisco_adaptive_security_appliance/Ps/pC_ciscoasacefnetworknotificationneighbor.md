#### Parser Content
```Java
{
Name = cisco-asa-cef-network-notification-neighbor
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%LDP-5-NBRCHG:""", """|LDP:NBRCHG|Neighbor|""" ]
  Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
    """({event_code}%[\s\w+-]+):""",
        """({protocol}LDP)"""
# neighbor_ip is removed
        """ad.message=({event_name}.*?(UP|DOWN))\s*(\(?({failure_reason}.*?)?\))?\said""",
  ]

cisco-system-info = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SS","yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss.SSS","epoch_sec"]
  Fields = [
     """({time}\d+ \w+ \d+ \d+:\d+:\d+)\s+\w+:\s+\%""",
    """({event_code}%\w+\-[^:]+)""",
    """\%[\w+-.]+:\s*({additional_info}[^\$]+?)\s*$"""
  
}
```