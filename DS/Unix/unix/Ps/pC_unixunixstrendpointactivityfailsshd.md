#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-fail-sshd
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """sshd[""", """]: """, """error:""" ]
  Fields = [
    """>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """(\d\d:|(\+|-))\d\d:\d\d (::ffff:)?({host}[\w\-.]+)\s""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """\ssshd\[\d+\]:\s*error:\s*({failure_reason}.+?)\s*$""",
  ]


}
```