#### Parser Content
```Java
{
Name = cisco-ftd-str-network-traffic-success-stub-2
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-302024""" ]
  Fields = [
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s*:\s*%FTD""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """ Inside:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)""",
    """ (Outside|VLAN\d{3}):\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)""",
    """({event_name}Built (backup|director) stub (UDP|TCP) connection)"""
   ]


}
```