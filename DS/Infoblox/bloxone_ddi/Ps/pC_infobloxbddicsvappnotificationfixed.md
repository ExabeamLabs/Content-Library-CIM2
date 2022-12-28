#### Parser Content
```Java
{
Name = infoblox-bddi-csv-app-notification-fixed
  ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd[""", """,Fixed,""" ]
  Fields = [
    """({host}\S+) dhcpd\[""",
    """\]: Forward map from ({dest_host}.+?) to ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s({result}\w+):\s({additional_info}[^"]+)""",
    """\]: [^:]+:({dest_ip}[A-Fa-f:\d.]+),({result}Fixed),[^,]*?,({dest_mac}[A-Fa-f:\d.]+)""",
  ]


}
```