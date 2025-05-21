#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-session-fail-discarded
  Vendor = Forcepoint
  Product = Forcepoint Next-Gen Firewall
  ParserVersion = v1.0.0
  TimeFormat = ["epoch","MMM dd yyyy HH:mm:ss"]
  Conditions = [ 
"""CEF:"""
"""|FORCEPOINT|"""
"""|Connection_Discarded|""" 
]
  Fields = [
    """ahost=\s*({host}.+?)(\s\w+=)""",
    """\Wrt=({time}\d{13})""",
    """src=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """dhost=\s*({dest_host}.+?)(\s\w+=)""",
    """dst=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s\w+=)""",
    """amac=\s*({src_mac}.+?)(\s\w+=)""",
    """dvc=\s*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s|({src_host}[\w\.\-]+))""",
    """app=\s*({protocol}.+?)(\s\w+=)""",
    """\Win=({bytes_in}\d+)""",
    """\Wout=({bytes_out}\d+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\sdeviceInboundInterface=({src_interface}.+?)\s*\w+=""",
    """\sdeviceOutboundInterface=({dest_interface}.+?)\s*\w+=""",
    """proto=\s*({protocol}.+?)(\s\w+=)"""
    """({operation}Connection_Discarded)"""
    """\Wrt=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  ]


}
```