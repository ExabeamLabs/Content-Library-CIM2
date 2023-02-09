#### Parser Content
```Java
{
Name = ruckus-r-kv-app-activity-success-filecatchsync
  Vendor = Ruckus
  Product = Ruckus
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:FileCache synced""" ]
  Fields = [
    """({event_name}FileCache synced)""",
    """pid=({process_id}[^,]+)""",
  ]


}
```