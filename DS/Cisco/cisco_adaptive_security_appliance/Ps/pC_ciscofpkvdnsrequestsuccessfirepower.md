#### Parser Content
```Java
{
Name = "cisco-fp-kv-dns-request-success-firepower"
Conditions = [
"""|Cisco|"""
"""|Firepower|"""
"""|CONNECTION STATISTICS|"""
"""destinationDnsDomain="""
]
ParserVersion = "v1.0.0"

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