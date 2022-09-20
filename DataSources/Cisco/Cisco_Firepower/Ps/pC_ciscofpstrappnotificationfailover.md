#### Parser Content
```Java
{
Name = cisco-fp-str-app-notification-failover
  Vendor = Cisco
  ParserVersion = "v1.0.0"
  Product = Cisco Firepower
  TimeFormat = "epoch_sec"
  Conditions = [ """Original Address=""", """failover""" ]
  Fields = [
    """\s({time}\d+)\.\d+\s""",
    """Original Address=({host}[^\s]+)\s""",
    """events\s*({event_name}.*?)\s*$""",
    """failover to ({src_interface}.*?)\s*$""",
  ]
  DupFields = ["host->src_host"]


}
```