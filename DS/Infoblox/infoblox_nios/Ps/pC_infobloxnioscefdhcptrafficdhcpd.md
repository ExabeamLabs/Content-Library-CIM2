#### Parser Content
```Java
{
Name = infoblox-nios-cef-dhcp-traffic-dhcpd
  Vendor = Infoblox
  Product = Infoblox NIOS
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """Infoblox_NIOS DHCP""", """dhcpd""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdmac=({dest_mac}[a-fA-F\d.:]+)""",
    """\|Infoblox_NIOS DHCP ({operation}[^\|]+)""",
    """CEF[^\|]+\|([^\|]*\|){4}({event_name}[^\|]+)""",
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\sCEF"""
  ]


}
```