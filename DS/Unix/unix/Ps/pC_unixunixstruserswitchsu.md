#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-su
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ su:""", """ BAD SU """, """ from """, """ to """ ]
  Fields = [
    """Message forwarded from (::ffff:)?({host}[^\s:]+)"""
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """\d\d:\d\d:\d\d (::ffff:)?({host}\S+)? su:""",
    """\ssu:\s*({additional_info}.+?)\s*$"""
    """({event_code}su)"""
    """from ({user}[\w\.\-\!\#\^\~]{1,40}\$?) to ({account}\w+) at ({process_dir}.*?)\?*\s*$"""

  ]
  ParserVersion = "v1.0.0"


}
```