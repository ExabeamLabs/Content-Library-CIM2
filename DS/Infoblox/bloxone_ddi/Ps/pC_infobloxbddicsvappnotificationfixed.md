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
    """\]: [^:]+:({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,({result}Fixed),[^,]*?,({dest_mac}[A-Fa-f:\d.]+)""",
  ]


}
```