#### Parser Content
```Java
{
Name = cisco-fp-str-app-notification-failover
  Vendor = Cisco
  ParserVersion = "v1.0.0"
  Product = Cisco Network Security
  TimeFormat = "epoch_sec"
  Conditions = [ """Original Address=""", """failover""" ]
  Fields = [
    """\s({time}\d{10})\.\d+\s""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """Original Address=({host}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))|({src_host}[\w-.]+)))\s""",
    """events\s*({event_name}.*?)\s*$""",
    """failover to ({src_interface}.*?)\s*$""",
  ]


}
```