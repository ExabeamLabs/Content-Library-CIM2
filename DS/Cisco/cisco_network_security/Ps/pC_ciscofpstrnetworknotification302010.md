#### Parser Content
```Java
{
Name = cisco-fp-str-network-notification-302010
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """-302010""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)""",
    """%FTD-({priority}\d+)-({event_code}\d+)"""
  ]


}
```