#### Parser Content
```Java
{
Name = "cisco-asa-str-app-notification-607001-1"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """%FTD-""", """-607001""", """ Pre-allocate SIP """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s""",
    """%FTD-({priority}\d+)-({event_code}\d+):\s*({event_name}Pre-allocate SIP)\s[\w\s]*?({protocol}\w+)\ssecondary channel""",
    """for\s*(({src_interface}\w+):)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
    """to\s*(({dest_interface}\w+):)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?"""
  ]


}
```