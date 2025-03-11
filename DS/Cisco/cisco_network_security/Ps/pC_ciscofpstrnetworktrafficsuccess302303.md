#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-302303"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
	"""%FTD"""
	"""-302303"""
	"""state-bypass connection"""
  ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d+)""",
    """\w+ \d+ \d{4} \d\d:\d\d:\d\d (::ffff:)?({host}[\w.\-]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """from\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)).+?to\s*({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+))"""
    """({event_name}Built ({protocol}TCP|UDP).+?connection)"""
	]
	DupFields = [
	"event_name->operation"
	  ]


}
```