#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-113008
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-113008""" ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)\s*\S*\s*:\s*%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """-113008:\s+({event_name}AAA transaction status ACCEPT)""",
    """user\s*=\s*({user}[^@,\s:"]+)(@({domain}[^@,\s:]+))?""",
    """user\s*=\s*(({email_address}[^\@"]+\@[^"|\s]+)|({user}[^"|\s]+))"""
  ]


}
```