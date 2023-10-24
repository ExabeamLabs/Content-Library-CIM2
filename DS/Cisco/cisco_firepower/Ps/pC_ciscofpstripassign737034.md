#### Parser Content
```Java
{
Name = cisco-fp-str-ip-assign-737034
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-737034""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """\sSession=({session_id}[^,]+)\s*""",
    """IPv(4|6) address:\s*({event_name}.+?)(\s*"|\s*$)""",
  ]


}
```