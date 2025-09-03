#### Parser Content
```Java
{
Name = cisco-fp-str-configuration-download-111001
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """-111001""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)""",
    """\s(({host}[\w.\-]+))\s+:\s*(\w+\s|%\w+\-)""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """%FTD\-\d+\-\d+:\s*({event_name}.*?)\s*("|$)""",
    ]


}
```