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
    """\[({time}\d+\/\w+\/\d+:\d+:\d+:\d+)""", """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+.*?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+(-|({protocol}[^\s"]+))\s+({cipher}[^\s"]+)\s+[^"]*?\s*"({alert_name}[^"]*?)\s*"\s+({result}\d+)""",
  ]
  DupFields = [ "protocol->alert_type" ]


}
```