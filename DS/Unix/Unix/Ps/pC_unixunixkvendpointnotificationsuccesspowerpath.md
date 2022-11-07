#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-notification-success-powerpath
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ PowerPath: """, """ MPAPI: """ ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)?\s({dest_ip}[^\s]+)\s*({host}[^\s]+)\s*PowerPath:""",
    """\sPowerPath:\s*({additional_info}.+?)\s*$""",
  ]


}
```