#### Parser Content
```Java
{
Name = cisco-fp-kv-radius-traffic-success-113004
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """-113004"""
  """%FTD-"""
  """AAA user authentication Successful"""
]
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)"""
  """%FTD-({priority}\d+)-({event_code}\d+)"""
  """server\s*=\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """-113004:\s*({event_name}AAA user authentication Successful)"""
  """user\s*=\s*(({email_address}[^@]+@[^\s]+)|({user}[^\s]+))"""
]
ParserVersion = "v1.0.0"


}
```