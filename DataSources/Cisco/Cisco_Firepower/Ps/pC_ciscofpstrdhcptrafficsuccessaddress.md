#### Parser Content
```Java
{
Name = cisco-fp-str-dhcp-traffic-success-address
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """Original Address=""", """dhcp""" ]
  Fields = [
    """\s({time}\d+)\.\d+\s""",
    """Original Address=({host}[^\s]+)\s""",
    """events\s*({event_name}.*?)\s*$""",
    """dhcp no offers for mac ({src_mac}.+?)\s*$""",
  ]
  DupFields = ["host->src_host"]


}
```