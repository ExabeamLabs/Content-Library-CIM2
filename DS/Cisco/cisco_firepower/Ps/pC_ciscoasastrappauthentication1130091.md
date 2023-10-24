#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-113009-1
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%FTD-auth-6-113009""" ]
  Fields = [
    """({time}\d+ \w+ \d+ \d+:\d+:\d+)""",
    """%FTD-\w+?-?({priority}\d+)-({event_code}\d+)""",
    """-113009:\s+({event_name}AAA retrieved default group policy)""",
    """user\s*=\s*({user}[\w\.\-]{1,40}\$?)(@({domain}[^@,\s:]+))?""",
  ]


}
```