#### Parser Content
```Java
{
Name = cisco-fp-str-configuration-modify-111004
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-111004""", """%FTD-""" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """%FTD\-({priority}\d+)\-({event_code}\d+):\s*({event_name}.+?)\s*($|")""",
  ]


}
```