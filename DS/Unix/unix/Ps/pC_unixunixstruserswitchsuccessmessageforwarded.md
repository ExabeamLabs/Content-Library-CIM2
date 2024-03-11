#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-success-messageforwarded
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" su: from """,
""" Message forwarded from """
  ]
  Fields = [
"""Message forwarded from (::ffff:)?({host}[^\s:]+)"""
"""({event_code}su)"""
"""su: from ({user}\w+) to ({account}\w+) at ({process_dir}.*?)\?*\s*$"""
  ]


}
```