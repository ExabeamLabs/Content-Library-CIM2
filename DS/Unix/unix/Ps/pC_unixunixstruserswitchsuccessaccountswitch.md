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
"""(T|\s)\d\d:\d\d:\d\d(\.?\S+)?\s+(::ffff:)?({host}[\w\.\-]+)?\s*({event_code}su):\s+\(to\s+({account}[^)]+)\)\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s+on""",
"""(T|\s)\d\d:\d\d:\d\d(\.?\S+)?\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.-]+))\s""",
  ]


}
```