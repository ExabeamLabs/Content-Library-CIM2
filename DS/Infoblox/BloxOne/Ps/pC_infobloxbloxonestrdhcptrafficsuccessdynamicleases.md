#### Parser Content
```Java
{
Name = infoblox-bloxone-str-dhcp-traffic-success-dynamicleases
  Vendor = Infoblox
  Product = BloxOne
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """ BOOTREQUEST from """, """BOOTP from dynamic client and no dynamic leases""" ]
  Fields = [
    """\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s+({host}[\w.-]+)\s+({src_ip}[A-Fa-f\d:.]+)\s+dhcpd\[""",
    """\sdhcpd\[\d+\]:\s+BOOTREQUEST from ({dest_mac}\S+) via ({dest_ip}[A-Fa-f:\d.]+?):?\s"""
  ]


}
```