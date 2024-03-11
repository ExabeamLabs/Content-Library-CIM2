#### Parser Content
```Java
{
Name = cisco-fp-str-app-notification-210007
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%FTD-""", """-210007""", """ failed """, """ dynamic-pat """ ]
  Fields = [
    """({time}[a-zA-Z]{1,3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """:\d\d:\d\d\s+({host}[\w\.-]+)\s*:\s*%FTD-""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}LU allocate xlate ({result}failed) for ((?i)(static|dynamic)-(nat|pat)) ({protocol}\w+) translation)""",
    """\sfrom\s+({src_interface}[^:]+?):({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?\s+\(({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_translated_port}\d+))?\)""",
    """\sto\s+({dest_interface}[^:]+?):({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?\s+\(({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_translated_port}\d+))?\)"""
  ]


}
```