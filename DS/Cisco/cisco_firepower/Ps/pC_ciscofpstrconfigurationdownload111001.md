#### Parser Content
```Java
{
Name = cisco-fp-str-configuration-download-111001
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-111001""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """%FTD\-\d+\-\d+:\s*({event_name}.*?)\s*("|$)""",
    ]


}
```