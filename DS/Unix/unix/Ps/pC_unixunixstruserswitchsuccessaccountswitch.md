#### Parser Content
```Java
{
Name = unix-unix-str-user-switch-success-accountswitch
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""su: (to""",
""" on """
  ]
  Fields = [
"""\d\d:\d\d\s+(::ffff:)?({host}[\w\.\-]+)?\s*({event_code}su):\s+\(to\s+({account}[^)]+)\)\s+({user}[\w\.]+)\s+on""",
""":\d\d:\d\d\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.-]+))\s""",
  ]


}
```