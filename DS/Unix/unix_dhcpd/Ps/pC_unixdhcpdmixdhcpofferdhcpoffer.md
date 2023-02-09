#### Parser Content
```Java
{
Name = unix-dhcpd-mix-dhcp-offer-dhcpoffer
  Vendor = Unix
  Product = Unix dhcpd
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd: """, """ DHCPOFFER """ ]
  Fields = [
    """DHCPOFFER on ({dest_ip}[A-Fa-f:\d.]+) to ({dest_mac}[A-Fa-f:\d.]+)\s*(\(({dest_host}[\w\-.]+)\))? via (({src_ip}[\da-fA-F.:]+[\da-fA-F]):?|({dest_interface}[^\s"]+))""",
    """\w{3} \d{1,2} \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+) dhcpd:""",
    """dhcpd:\s*({event_name}\S+)""",
  ]


}
```