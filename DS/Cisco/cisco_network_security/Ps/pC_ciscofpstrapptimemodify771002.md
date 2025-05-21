#### Parser Content
```Java
{
Name = cisco-fp-str-app-time-modify-771002
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """-771002""", """%FTD-""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}CLOCK: System clock set)"""
  ]


}
```