#### Parser Content
```Java
{
Name = cisco-asa-kv-radius-traffic-success-113004
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "yyyy MMM dd HH:mm:ss"
Conditions = [
  """%FTD-auth-6-113004:"""
  """AAA user authentication Successful"""
]
Fields = [
  """({time}\d+ \w+ \d+ \d+:\d+:\d+)"""
  """%FTD-\w+?-?({priority}\d+)-({event_code}\d+)"""
  """-113004:\s+({event_name}AAA user authentication Successful)"""
  """: user\s*=? ({user}[^\s]+)"""
  """server =\s+({dest_ip}[A-Za-z\d.:]+)"""
]
ParserVersion = "v1.0.0"


}
```