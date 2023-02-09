#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-113009
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-113009""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d):\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """-113009:\s+({event_name}AAA retrieved default group policy)""",
    """user\s*=\s*({user}[^@,\s:"]+)(@({domain}[^@,\s:]+))?""",
    """user\s*=\s*(({email_address}[^\@"]+\@[^"|\s]+)|({user}[^"|\s]+))"""
  ]


}
```