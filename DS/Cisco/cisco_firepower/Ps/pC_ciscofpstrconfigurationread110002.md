#### Parser Content
```Java
{
Name = cisco-fp-str-configuration-read-110002
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-110002""", """%FTD-""", """Failed """ ]
  Fields = [
    """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """({host}[\w.\-]+)\s+:?\s*%FTD-""",
    """%FTD-({priority}\d+)-({event_code}\d+):\s*({event_name}.*?)\sfor\s*({protocol}\w+)\s""",
    """\sfrom\s*(({src_interface}\w+):({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))\/({=src_port}\d+)""",
    """\sto\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))\/({=dest_port}\d+)""",
  ]


}
```