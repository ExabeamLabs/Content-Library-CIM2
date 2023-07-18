#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-login-success-httpd
  ParserVersion = "v1.0.0"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""" httpd:"""
"""]: Login_Allowed - """
"""apparently_via="""
  ]
  Fields = [
"""httpd:\s*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
"""\d\d:\d\d:\d\d(\.\S+)?\s({host}[\w\-.]+)""",
"""\w+\s+\d+\s+\d+:\d+:\d+(\.\S+)?\s+({host}[\w\-.]+)\s+""",
"""ip=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s"""
"""group=({group_name}[^\s\"]+)"""
"""auth=({auth_method}[^\s]+)"""
"""\[(-|(({domain}[^\\\]]+)\\{1,25})?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\]:\s*({event_name}Login_Allowed)"""
  ]


}
```