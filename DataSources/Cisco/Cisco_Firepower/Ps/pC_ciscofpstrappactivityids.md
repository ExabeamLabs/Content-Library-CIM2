#### Parser Content
```Java
{
Name = cisco-fp-str-app-activity-ids
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """Original Address=""", """IDS""" ]
  Fields = [
    """\s({time}\d+)\.\d+\s""",
    """Original Address=({host}[^\s]+)\s""",
    """events\s*({event_name}.*?)\s*$""",
    """IDS:\s*({additional_info}.*?)\s*$""",
  ]
  DupFields = ["host->src_host"]


}
```