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
    """\]: ({event_name}DHCPEXPIRE) on ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? to ({src_mac}[A-Fa-f:\d.]+)""",
  ]


}
```