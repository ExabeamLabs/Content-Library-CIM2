#### Parser Content
```Java
{
Name = unix-unix-str-scheduled-task-start-crond
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """crond[""", """]: """, """cmd""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(.\d+)?Z)\s(::ffff:)?({host}[\w\-.]+)\s""",
    """({time}\w+\s+\d{2}\s+\d{2}:\d{2}:\d{2})\s*({host}[\w.\-]+)\s""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? crond\[""",
    """\scrond\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """USER\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*pid""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
    """(::ffff:)?({host}\S+)\sCROND"""
  ]


}
```