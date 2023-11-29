#### Parser Content
```Java
{
Name = cisco-fp-str-network-session-fail-710005
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD""", """-710005""", """request discarded""" ]
  Fields = [
      """({time}\w+\s\d\d\s\d{4}\s\d\d:\d\d:\d\d)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """({event_name}({protocol}TCP|UDP)\s+({action}request ({result}discarded)))""",
      """\sfrom\s+({src_ip}[.:a-fA-F\d]+)\/({src_port}\d+)""",
      """\sto\s\S+\:({dest_ip}[.:a-fA-F\d]+)\/({dest_port}\d+)""",
      """to\s*({dest_interface}\w+):({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)"""
  ]
  DupFields = [
	"event_name->operation"
  ]


}
```