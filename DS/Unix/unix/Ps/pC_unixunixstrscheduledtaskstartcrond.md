#### Parser Content
```Java
{
Name = unix-unix-str-scheduled-task-start-crond
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """crond[""", """]: """, """cmd""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? crond\[""",
    """\scrond\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """USER\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*pid"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]


}
```