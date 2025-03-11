#### Parser Content
```Java
{
Name = cisco-fp-str-certificate-validate-717022
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-717022""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """cn=({full_name}[^,]+),ou=""",
    """subject name:\s*e=({email_address}[^@]+@[^.]+\.[^,]+)"""
    """({event_name}Certificate was successfully validated)"""
  ]


}
```