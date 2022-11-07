#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-su
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ su:""", """ from """, """ to """ ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? su:""",
    """\ssu:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```