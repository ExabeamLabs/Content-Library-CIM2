#### Parser Content
```Java
{
Name = unix-dhcpd-str-dhcp-acknowledge-dhcpack
  ParserVersion = v1.0.0
  Conditions = [ """ dhcpd: DHCPACK """ ]
  Fields = ${DHCPDParsersTemplates.dhcpd-events.Fields}[
    """DHCPACK to ({dest_ip}[a-fA-F\d.:]+) \(({dest_mac}[a-fA-F\d.:]+)\) via (({src_ip}[\d.:a-fA-F]+[\da-fA-F]):?|({dest_interface}[^\s"]+))""",
    """DHCPACK on ({dest_ip}[a-fA-F\d.:]+) to ({dest_mac}[a-fA-F\d.:]+)(\s+\(({dest_host}[\w\-.]+)\))? via (({src_ip}[\d.:a-fA-F]+[\da-fA-F]):?|({dest_interface}[^\s"]+))""",
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