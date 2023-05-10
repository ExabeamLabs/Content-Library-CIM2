#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-traffic-success-dhcpd
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPINFORM from """ ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """({event_name}DHCPINFORM) from ({dest_ip}[A-Fa-f:\d.]+) via ({dest_interface}[^\s"]+)\sTransID\s({trans_id}\w+)""",
  ]
  ParserVersion = "v1.0.0"


}
```