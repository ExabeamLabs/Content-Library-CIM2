#### Parser Content
```Java
{
Name = vmware-esxi-str-app-logout-loggedout
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""" logged out """,""" [User ""","""Event [""",""" vpxd """ ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({host}[^\s]+)\s""",
    """User\s+((({domain}[^\\\s@]+)[\\\/]+)?({user}[^\s\\@]+)).+?\s*logged""",
    """\[({event_name}User.+?logged (out|in))""",
    """user agent:\s+({user_agent}[^)]+)"""
    """\w+@(127.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  ]


}
```