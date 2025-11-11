#### Parser Content
```Java
{
Name = cisco-fp-str-network-close-success-302304
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-302304""", """%FTD-""", """state-bypass connection""", """Connection timeout""" ]
  Fields = [
    """({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
	  """%FTD-({priority}\d+)-({event_code}\d+)"""
    """({event_name}({action}Teardown)\s+({protocol}[^\s]+).+?connection)""",
    """from\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)).+?to\s*({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+))"""
	  """\sduration\s+({duration}\S+)\s+bytes\s+({bytes}\d+)(\s+({result_reason}[^\("]+[^\(\s"])\s)?"""
    """({operation}({action}Teardown)\s+({protocol}[^\s]+).+?connection)""",
  ]


}
```