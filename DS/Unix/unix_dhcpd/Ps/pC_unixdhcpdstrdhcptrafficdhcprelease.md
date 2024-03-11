#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-traffic-dhcprelease
  ParserVersion = v1.0.0
  Conditions = [ """ dhcpd: """, """ DHCPRELEASE """ ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """DHCPRELEASE of ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+)) from ({dest_mac}[A-Fa-f:\d.]+)\s*(\(({dest_host}[\w\-.]+)\))? via ({dest_interface}[^\s"]+)""",
  ]

dhcpd-events = {
  Vendor = Unix
  Product = Unix dhcpd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\w{3} \d{1,2} \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+) dhcpd:""",
    """dhcpd:\s*({event_name}\S+)""",
  
}
```