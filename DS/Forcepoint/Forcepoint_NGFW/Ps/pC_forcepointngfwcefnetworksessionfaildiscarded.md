#### Parser Content
```Java
{
Name = forcepoint-ngfw-cef-network-session-fail-discarded
  Vendor = Forcepoint
  Product = Forcepoint NGFW
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ 
"""CEF:"""
"""|FORCEPOINT|"""
"""|Connection_Discarded|""" 
]
  Fields = [
    """CEF:\s+\d+\|([^\|]+\|){4}({operation}[^\|]+)""",
    """ahost=\s*({host}.+?)(\s\w+=)""",
    """\Wrt=({time}\d+)""",
    """src=\s*({src_ip}[A-Za-z\d.:]+)\s""",
    """dhost=\s*({dest_host}.+?)(\s\w+=)""",
    """dst=\s*({dest_ip}.+?)(\s\w+=)""",
    """amac=\s*({src_mac}.+?)(\s\w+=)""",
    """dvc=\s*({src_host}.+?)(\s\w+=)""",
    """app=\s*({protocol}.+?)(\s\w+=)""",
    """\Win=({bytes_in}\d+)""",
    """\Wout=({bytes_out}\d+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\sdeviceInboundInterface=({src_interface}.+?)\s*\w+=""",
    """\sdeviceOutboundInterface=({dest_interface}.+?)\s*\w+=""",
    """proto=\s*({protocol}.+?)(\s\w+=)"""
  ]


}
```