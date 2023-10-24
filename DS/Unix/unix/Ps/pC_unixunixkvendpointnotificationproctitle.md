#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-notification-proctitle
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "epoch_sec"
  Conditions = [ """type=PROCTITLE """, """ proctitle=""" ]
  Fields = [
    """msg=audit\(({time}\d{10})""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\w+:""",
# node is removed
    """type=({event_category}[^=]+?)\s+(\w+=|$)""",
    """msg=({event_name}[^=]+?)\s+(\w+=|$)""",
    """type=({event_name}PROCTITLE)""",
# proctitle is removed
  ]


}
```