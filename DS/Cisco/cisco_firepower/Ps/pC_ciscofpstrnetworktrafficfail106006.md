#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-fail-106006"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%FTD-""", """-106006""", """Deny """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """from\s*(({src_interface}\w+):)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
    """to\s*(({dest_interface}\w+):)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
    """({event_name}({action}Deny)\s\S+\s+({protocol}\w+))""",
    """on interface\s*({dest_interface}[^"]+?)(\s*"|\s*$)""",
  ]


}
```