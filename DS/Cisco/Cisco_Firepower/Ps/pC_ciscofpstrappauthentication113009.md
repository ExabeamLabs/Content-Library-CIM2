#### Parser Content
```Java
{
Name = cisco-fp-str-app-authentication-113009
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
  """-113009"""
  """%FTD-"""
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """server\s*=\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """-113009:\s+({event_name}AAA retrieved default group policy)"""
    """user\s*=\s*({user}[^@,\s:"]+)(@({email_domain}[^@,\s:]+))?"""
  ]


}
```