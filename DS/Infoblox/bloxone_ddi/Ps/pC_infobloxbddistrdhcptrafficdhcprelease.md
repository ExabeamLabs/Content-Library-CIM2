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
    """({event_name}DHCPRELEASE) of ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? from ({dest_mac}[A-Fa-f:\d.]+)\s*(\(({dest_host}[\w\-.]+)\))? via ({dest_interface}[^\s"]+).*TransID\s({trans_id}\w+)""",
  ]


}
```