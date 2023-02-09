#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-success-cron
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """cron[""", """]: """ ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d(\.\S+)?\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d(\.\S+)? (::ffff:)?({host}\S+)? f?cron\[""",
    """cron\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]


}
```