#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-traffic-dhcpinform
  ParserVersion = v1.0.0
  Conditions = [ """ dhcpd""", """ DHCPINFORM """ ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """({event_name}DHCPINFORM) from ({dest_ip}[A-Fa-f:\d.]+) via (({src_ip}[\d.:a-fA-F]+[\da-fA-F]):?|({dest_interface}[\w-]+))""",
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