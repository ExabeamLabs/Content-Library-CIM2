#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-discoverdhcpd
  ParserVersion = v1.0.0
  Conditions = [ """ dhcpd: """, """ DHCPDISCOVER """ ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """({event_name}DHCPDISCOVER) from ({dest_mac}[A-Fa-f:\d.]+)(\s+\(({dest_host}[\w\-.]+)\))? via (({dest_ip}[\d.:a-fA-F]+[\da-fA-F]):?|({dest_interface}[^\s"]+))""",
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