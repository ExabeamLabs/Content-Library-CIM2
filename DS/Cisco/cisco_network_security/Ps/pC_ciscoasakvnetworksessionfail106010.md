#### Parser Content
```Java
{
Name = cisco-asa-kv-network-session-fail-106010
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%FTD-""", """-106010""", """Deny """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}({action}Deny) inbound protocol)""",
    """src\s*(({src_interface}\w+):)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
    """dst\s*(({dest_interface}\w+):)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
  ]


}
```