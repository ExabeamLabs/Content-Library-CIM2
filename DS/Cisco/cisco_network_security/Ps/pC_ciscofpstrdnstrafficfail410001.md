#### Parser Content
```Java
{
Name = cisco-fp-str-dns-traffic-fail-410001
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """%FTD-""", """-410001""" ]
  Fields = [
    """({time}\w+ \d+ (\d+ )?\d\d:\d\d:\d\d)\s*(\w+\s)?(::ffff:)?({host}[\w\-.]+)?\s*""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
	  """%FTD-\d+-\d+:\s*({event_name}[^:].+?)\s+from"""
	  """({protocol}ICMP|TCP|UDP)"""
	  """({action}Dropped)"""
    """from\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)).+?to\s*({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+))"""
  ]


}
```