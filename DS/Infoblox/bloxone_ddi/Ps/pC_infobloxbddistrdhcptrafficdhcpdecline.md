#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-traffic-dhcpdecline
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPDECLINE of """ ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """({event_name}DHCPDECLINE) of ({dest_ip}[A-Fa-f:\d.]+)\sfrom\s({dest_mac}[`A-Fa-f:\d.]+)\s(\([^\)]+\)\s)?via\s({dest_interface}[A-Fa-f:\d.]+)\sTransID\s({trans_id}[^\s:]+):?( not found)?""",
  ]


}
```