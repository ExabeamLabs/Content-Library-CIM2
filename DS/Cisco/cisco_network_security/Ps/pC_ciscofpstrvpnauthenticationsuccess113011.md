#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-authentication-success-113011
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy MMM dd HH:mm:ss","MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """%FTD-auth-6-113011:""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)"""
    """({time}\d+ \w+ \d+ \d+:\d+:\d+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-\w+?-?({priority}\d+)-({event_code}\d+)""",
    """-113011:\s+({event_name}AAA retrieved user specific group policy)""",
    """for user\s*=? (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    ]


}
```