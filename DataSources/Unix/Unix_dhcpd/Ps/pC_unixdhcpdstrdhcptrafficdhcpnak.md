#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-traffic-dhcpnak
  ParserVersion = v1.0.0
  Conditions = [ """ dhcpd: """, """ DHCPNAK """ ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """DHCPNAK on ({dest_ip}[A-Fa-f:\d.]+) to ({dest_mac}[A-Fa-f:\d.]+) via ({dest_interface}[^\s"]+)""",
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