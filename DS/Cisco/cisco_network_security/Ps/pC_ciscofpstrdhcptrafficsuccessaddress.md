#### Parser Content
```Java
{
Name = cisco-fp-str-dhcp-traffic-success-address
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """Original Address=""", """dhcp""" ]
  Fields = [
    """\s({time}\d{10})\.\d+\s""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """Original Address=({host}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))|({src_host}[\w-.]+)))\s""",
    """events\s*({event_name}.*?)\s*$""",
    """dhcp no offers for mac ({src_mac}.+?)\s*$""",
  ]


}
```