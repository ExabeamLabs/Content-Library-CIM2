#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-success-su
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""succeeded for""",
""" su:"""
  ]
  Fields = [
"""\d\d:\d\d\s*(::ffff:)?({host}[\w\.\-]+)?\s*({event_code}su):\s(?:\[[^]]+\])?\s*\'su ({dest_user}[^']+)\' succeeded for\s+({user}[\w\.]+)\s+on"""
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s"""
  ]


}
```