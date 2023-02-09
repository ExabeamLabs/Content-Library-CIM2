#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-traffic-dhcprelease
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPRELEASE of""" ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """({event_name}DHCPRELEASE) of ({dest_ip}[A-Fa-f:\d.]+) from ({dest_mac}[A-Fa-f:\d.]+)\s*(\(({dest_host}[\w\-.]+)\))? via ({dest_interface}[^\s"]+).*TransID\s({trans_id}\w+)""",
  ]


}
```