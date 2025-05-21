#### Parser Content
```Java
{
Name = cisco-fp-str-configuration-delete-110003
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """-110003""", """%FTD-""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s""",
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)""",
    """\s(({host}[\w.\-]+))\s+:\s*(\w+\s|%\w+\-)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\sfrom\s*(({src_interface}[^:]+):)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({src_port}\d+)""",
    """-110003:\s({event_name}.+?)\s*for\s*({protocol}[^\s]+)""",
    """\d+\sto\s*(({dest_interface}[^:]+):)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({dest_port}\d+)"""
  ]


}
```