#### Parser Content
```Java
{
Name = infoblox-bddi-csv-ip-free-dhcpd
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """,Freed,""" ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """\]: Forward map from ({dest_host}.+?) to ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s({result}\w+):\s({additional_info}[^"]+)""",
    """\]: [^:]+:({dest_ip}[A-Fa-f:\d.]+),({result}Freed),[^,]*?,({dest_mac}[A-Fa-f:\d.]+)""",
  ]


}
```