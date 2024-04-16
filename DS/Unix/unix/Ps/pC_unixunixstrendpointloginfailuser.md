#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-user"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [
""" httpd:"""
"""AD authentication for user"""
"""failed"""
  ]
  Fields = [
"""({time}\w+\s\d+\s\d\d:\d\d:\d\d(\.\S+)?)\s({host}[^\s]+)""",
"""@timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""\w+\s+\d+\s+\d+:\d+:\d+(\.\S+)?\s+({host}[\w\-.]+)\s+""", 
"""\w+\s+\d+\s+\d+:\d+:\d+(\.\S+)?\s+[A-Fa-f:\d\.]+\s\w+:\s*({host}[\w\-]+)""",
"""({event_name}AD authentication) for user ({user}[\w\.\-]{1,40}\$?) ({result}failed)"""
  ]
  ParserVersion = "v1.0.0"


}
```