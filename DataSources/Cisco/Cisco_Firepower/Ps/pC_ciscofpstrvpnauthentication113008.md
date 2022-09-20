#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-authentication-113008
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ 
  """%FTD-auth-6-113008:"""
  ]
  Fields = [
    """({time}\d+ \w+ \d+ \d+:\d+:\d+)"""
    """%FTD-\w+?-?({priority}\d+)-({event_code}\d+)"""
    """-113008:\s+({event_name}AAA transaction status ACCEPT)"""
    """ user\s*=? ({user}[^\s]+)"""
    ]


}
```