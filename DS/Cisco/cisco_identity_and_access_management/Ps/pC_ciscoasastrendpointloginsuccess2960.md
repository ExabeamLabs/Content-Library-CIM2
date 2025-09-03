#### Parser Content
```Java
{
Name = cisco-asa-str-endpoint-login-success-2960
  ParserVersion = "v1.0.0"
  Conditions = [
"""%DOT1X-5-SUCCESS:"""
"""Authentication successful"""
]

cisco-2960-auth-events = {
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd yyyy HH:mm:ss.SSS", "MMM dd HH:mm:ss", "MMM dd HH:mm:ss.SSS Z","MMM dd HH:mm:ss.SSS z", "MMM dd yyyy HH:mm:ss.SSS z", "MMM dd yyyy HH:mm:ss.SSS Z"]
  Fields = [
"""\d+:\s*({host}[\w\-\.]+)(:\s*\d+)?:\s*\w+\s\d+\s(\d\d\d\d\s)?\d\d:\d\d:\d\d(\.\d+)?(\s*\w+)?:\s*%\w+-"""
"""\w+\s\d+\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s"""
"""\s({time}\w+ \d+ \d+:\d+:\d+)"""
""" for client \(({src_mac}[^\)]+)\) on Interface ({src_interface}\S+) """
"""%({event_code}\w+\-\d+\-({result}[^:]+))"""
"""({event_name}Authentication \w+)"""
"""\s({time}\w{3}\s+\d{2}\s+\d\d:\d\d:\d\d\.\d+\s+\w+)"""
"""({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d\d\d(\s+\w+)?)"""
  
}
```