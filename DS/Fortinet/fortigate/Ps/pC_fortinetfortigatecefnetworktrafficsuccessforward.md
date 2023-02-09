#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-network-traffic-success-forward
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "epoch"
  Conditions = [ """|Fortinet|Fortigate|""", """FTNTFGTeventtime=""", """FTNTFGTdstintfrole=""", """|traffic:forward """, """FTNTFGTsubtype=forward""" ]
  Fields = [
    """FTNTFGTeventtime=({time}\d{13})""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)""",
    """\sshost=(({src_ip}[a-fA-F\d\.]+)|({src_host}[^\s]+?))\s\w+=""",
    """\ssrc=({src_ip}[a-fA-F\d\.]+)""",
    """\sspt=({src_port}\d{1,5})""",
    """\sdhost=(({dest_ip}[a-fA-F\d\.]+)|({dest_host}[^\s]+?))\s\w+=""",
    """\sdst=({dest_ip}[a-fA-F\d\.]+)""",
    """\sdpt=({dest_port}\d{1,5})""",
    """\sact=({action}[^=]+?)\s\w+=""",
    """\sout=({bytes_out}\d+)""",
    """\sin=({bytes_in}\d+)""",    
    """\|Fortinet\|Fortigate\|([^|]+\|){2}({event_name}[^|]+)\|""",
    """deviceInboundInterface=({src_interface}[^=]+?)\s\w+=""",
    """deviceOutboundInterface=({dest_interface}[^=]+?)\s\w+=""",
    """\sproto=({protocol}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```