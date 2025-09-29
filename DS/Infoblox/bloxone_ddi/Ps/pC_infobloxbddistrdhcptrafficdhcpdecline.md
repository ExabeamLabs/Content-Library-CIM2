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
    """({event_name}DHCPDECLINE) of ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\sfrom\s({dest_mac}[`A-Fa-f:\d.]+)\s(\([^\)]+\)\s)?via\s({dest_interface}[A-Fa-f:\d.]+)\sTransID\s({transaction_id}[^\s:]+):?( not found)?""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [ "transaction_id->trans_id"]


}
```