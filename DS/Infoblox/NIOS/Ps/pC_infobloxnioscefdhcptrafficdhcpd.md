#### Parser Content
```Java
{
Name = infoblox-nios-cef-dhcp-traffic-dhcpd
  Vendor = Infoblox
  Product = NIOS
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """Infoblox_NIOS DHCP""", """dhcpd""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdmac=({dest_mac}[a-fA-F\d.:]+)""",
    """\|Infoblox_NIOS DHCP ({operation}[^\|]+)""",
    """CEF[^\|]+\|([^\|]*\|){4}({event_name}[^\|]+)""",
    """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\sCEF"""
  ]


}
```