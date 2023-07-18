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
  """: user\s*=?\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\-\.]{1,40}))"""
  """server =\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```