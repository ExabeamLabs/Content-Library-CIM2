#### Parser Content
```Java
{
Name = f5-bigipasm-str-app-notification-infologger
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Application Security Manager
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss"
  Conditions = [ """ info logger: """ , """ [ssl""" , """ -""" , """] """, """"/"""]
  Fields = [
    """\[({time}\d+\/\w+\/\d+:\d+:\d+:\d+)""", """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+.*?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+(-|({protocol}[^\s"]+))\s+({cipher}[^\s"]+)\s+[^"]*?\s*"({alert_name}[^"]*?)\s*"\s+({result}\d+)""",
  ]
  DupFields = [ "protocol->alert_type" ]


}
```