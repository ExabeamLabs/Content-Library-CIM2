#### Parser Content
```Java
{
Name = watchguard-w-str-app-notification-appinfo
  ParserVersion = "v1.0.0"
  Vendor = Watchguard
  Product = Watchguard
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """https-proxy[""", """fail to get app info""" ]
  Fields = [
    """(({host}[\w.\-]+)\s+)?\(({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\s*\d\d)\)\s+""",
    """\s({event_code}https-proxy\[\d+\]):\s*({event_name}.+)\s"""
  ]


}
```