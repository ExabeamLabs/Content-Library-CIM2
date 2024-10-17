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
    """User\s+((({domain}[^\\\s@]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)).+?\s*logged""",
    """({event_name}logged (out|in))""",
    """user agent:\s+({user_agent}[^)]+)"""
    """\w+@(127.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]


}
```