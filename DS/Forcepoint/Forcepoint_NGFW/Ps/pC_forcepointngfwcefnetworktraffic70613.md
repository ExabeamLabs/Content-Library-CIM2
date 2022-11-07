#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-traffic-70613
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|FORCEPOINT|Firewall|""","""|70613|TCP_Segment-Invalid|""" ]

forcepoint-template-1= {
  Vendor = Forcepoint
  Product = Forcepoint NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields=[
    """\Wrt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host_ip}[A-Fa-f\d:.]+)""",
    """act=({action}[^=]+)\s\w+=""",
    """src=({src_ip}[A=Fa-f\d:.]+)""",
    """dst=({dest_ip}[A=Fa-f\d:.]+)""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """proto=({protocol}[^=]+?)\s\w+=""",
    """CEF:([^|]*\|){4}({event_code}[^|]+?)\|({event_name}[^|]+)\|""",
    """msg=({additional_info}[^"]+?)\s+\w+=""",
    """\Wout=({bytes_out}\d+)""",
    """\Win=({bytes_in}\d+)""",
    """deviceInboundInterface=({src_interface}[^=]+)\s\w+=""",
    """deviceOutboundInterface=({dest_interface}[^=]+)\s\w+="""
    ]
 
}
```