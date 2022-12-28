#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-success-unixid
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ unix:""", """ [ID""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d(\.\S+)?\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d(\.\S+)? (::ffff:)?({host}\S+)? unix:""",
    """\sunix:\s*({additional_info}.+?)\s*$"""
  ]


}
```