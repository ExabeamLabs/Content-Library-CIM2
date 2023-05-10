#### Parser Content
```Java
{
Name = hp-aruba-str-app-notification-success-sapd
  Vendor = Aruba
  Product = Aruba
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ sapd[""", """An internal system error has occurred""" ]
  Fields = [
    """({time}\w{3}\s+\d{2}\s+\d{2}:\d{2}:\d{2}\s+\d{4})\s+({src_ip}[A-Fa-f:\d.]+)\ssapd\[""",
    """sapd\|\s*({additional_info}An internal system error has occurred at file messenger.[^=]+?)\s({event_name}Unable to get [^"]+)\s(for|on interface)\s({src_interface}\S+?)\."""
  ]


}
```