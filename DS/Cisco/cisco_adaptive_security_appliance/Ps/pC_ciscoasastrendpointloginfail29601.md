#### Parser Content
```Java
{
Name = cisco-asa-str-endpoint-login-fail-2960-1
  ParserVersion = "v1.0.0"
  Conditions = [
"""%DOT1X-5-FAIL:"""
"""Authentication failed"""
]

cisco-2960-auth-events = {
  Vendor = "Cisco"
  Product = "Cisco Adaptive Security Appliance"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
""" for client \(({src_mac}[^\)]+)\) on Interface ({src_interface}\S+) """
"""%({event_code}\w+\-\d+\-({result}[^:]+))"""
"""({event_name}Authentication \w+)"""
  
}
```