#### Parser Content
```Java
{
Name = cisco-fp-str-user-modify-113003
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = v1.0.0
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%FTD-auth-6-113003:""" ]
  Fields = [
    """({time}\d+ \w+ \d+ \d+:\d+:\d+)""",
    """%FTD-\w+?-?({priority}\d+)-({event_code}\d+)""",
    """-113003:\s+({event_name}AAA group policy)""",
    """for user ({user}[^\s]+)"""
    ]


}
```