#### Parser Content
```Java
{
Name = cisco-fp-str-user-modify-113003
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%FTD-auth-6-113003:""" ]
  Fields = [
    """({time}\d+ \w+ \d+ \d+:\d+:\d+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-\w+?-?({priority}\d+)-({event_code}\d+)""",
    """-113003:\s+({event_name}AAA group policy)""",
    """for user (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    ]


}
```