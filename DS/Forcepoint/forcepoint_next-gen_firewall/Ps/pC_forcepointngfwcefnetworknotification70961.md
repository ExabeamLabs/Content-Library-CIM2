#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-notification-70961
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|FORCEPOINT|Firewall|""","""|70961|Connection_Rematched|""" ]

forcepoint-template-1= {
  Vendor = Forcepoint
  Product = Forcepoint Next-Gen Firewall
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields=[
    """\Wrt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """act=({action}[^=]+)\s\w+=""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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