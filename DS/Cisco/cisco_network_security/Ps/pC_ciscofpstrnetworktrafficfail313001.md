#### Parser Content
```Java
{
Name = cisco-fp-str-network-traffic-fail-313001
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-313001""", """%FTD-""", """Denied """ ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d) (::ffff:)?({host}[\w\-.]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Denied ({protocol}\w+))\s""",
    """\sfrom\s*((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))\s*on interface\s({src_interface}\w+)"""
  ]


}
```