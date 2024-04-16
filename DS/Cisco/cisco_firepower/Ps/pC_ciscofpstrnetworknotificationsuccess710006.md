#### Parser Content
```Java
{
Name = cisco-fp-str-network-notification-success-710006
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-710006""" ]
  Fields = [
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """%FTD-\d+-\d+:\s*({event_name}[^:].+?)\s+from"""
    """from\s+(({src_interface}.+?):)?((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?) to ({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))?)""",
    """({protocol}ICMP|TCP|UDP|SCPS)"""
  ]


}
```