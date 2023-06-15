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
    """DHCPOFFER on ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? to ({dest_mac}[A-Fa-f:\d.]+)\s*(\(({dest_host}[\w\-.]+)\))? via (({src_ip}[\da-fA-F.:]+[\da-fA-F]):?|({dest_interface}[^\s"]+))""",
    """\w{3} \d{1,2} \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+) dhcpd:""",
    """dhcpd:\s*({event_name}\S+)""",
  ]


}
```