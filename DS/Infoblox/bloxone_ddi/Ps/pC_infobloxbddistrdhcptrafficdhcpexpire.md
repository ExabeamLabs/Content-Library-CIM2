#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-traffic-dhcpexpire
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPEXPIRE on""" ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """\]: ({event_name}DHCPEXPIRE) on ({dest_ip}[A-Fa-f:\d.]+) to ({dest_mac}[A-Fa-f:\d.]+)""",
  ]


}
```