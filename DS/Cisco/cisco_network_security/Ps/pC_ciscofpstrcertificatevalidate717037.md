#### Parser Content
```Java
{
Name = cisco-fp-str-certificate-validate-717037
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-717037""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """subject name: e=({email_address}[^@]+@[^\.]+[^,]+)""",
    """cn=({full_name}[^,]+),ou="""
    """({event_name}Tunnel group search using certificate maps failed for peer certificate)"""
    ]


}
```