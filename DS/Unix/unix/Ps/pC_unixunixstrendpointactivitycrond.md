#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-crond
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """crond[""", """]: """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z\s(::ffff:)?({host}[\w\-.]+)\s""",
    """({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*(::ffff:)?({host}[\w\-\.]+)?(\s\w+)?\s*crond\[""",
    """\scrond\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]


}
```