#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-discover-dhcpd
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPDISCOVER from """ ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """({event_name}DHCPDISCOVER) from ({dest_mac}[A-Fa-f:\d.]+)(\s+\(({dest_host}[\w\-.]+)\))? via ({dest_interface}[^\s:"]+)(\sTransID\s({transaction_id}\w+))?""",
  ]
  DupFields = [ "transaction_id->trans_id"]


}
```