#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-requestdiscarded
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """%ASA""", """-710005""", """request discarded""" ]
  Fields = [
        """({time}\w+\s\d\d\s\d{0,4}\s*\d\d:\d\d:\d\d)""",
        """%ASA-({priority}\d+)-({event_code}\d+)""",
        """%ASA-[^\s]+\s({protocol}\w+)""",
        """({action}request ({result}discarded))""",
        """\sfrom\s+({src_ip}[.:a-fA-F\d]+)\/({src_port}\d+)""",
        """\sto\s\S+\:({dest_ip}[.:a-fA-F\d]+)\/({dest_port}\d+)""",
  ]


}
```