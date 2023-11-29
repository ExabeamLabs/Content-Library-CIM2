#### Parser Content
```Java
{
Name = cisco-fp-str-network-notification-success-500003
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-500003""" ]
  Fields = [
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """%FTD-\d+-\d+:\s*({event_name}[^:].+?)\s+from""",
    """from ((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)).+?to ((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+))(,.*? on interface ({dest_interface}\S+)|\s*"|\s*$)""",
    """({protocol}ICMP|TCP|UDP)"""
  ]


}
```