#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-sshd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","MMM dd HH:mm:ss"]
  Conditions = [ """sshd[""", """]: """ ]
  Fields = [
    """>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[-+]\d+:\d+)\s*(::ffff:)?({host}[\w\-.]+)\ssshd\["""
    """({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*(::ffff:)?({host}\S+)? sshd\[""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]


}
```