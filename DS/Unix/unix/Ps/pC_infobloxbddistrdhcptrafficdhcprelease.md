#### Parser Content
```Java
{
Name = infoblox-bddi-str-dhcp-traffic-dhcprelease
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """]: DHCPRELEASE of""" ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """({event_name}DHCPRELEASE) of ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? from ({src_mac}[A-Fa-f:\d.]+)\s*(\(({src_host}[\w\-.]+)\))? via ({src_interface}[^\s"]+).*TransID\s({transaction_id}\w+)""",
    """({event_name}DHCPRELEASE)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [ "transaction_id->trans_id"]


}
```