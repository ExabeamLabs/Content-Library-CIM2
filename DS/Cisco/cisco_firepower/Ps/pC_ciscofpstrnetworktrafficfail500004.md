#### Parser Content
```Java
{
Name = cisco-fp-str-network-traffic-fail-500004
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%FTD-""", """-500004""" ]
  Fields = [
    """({time}\w{3} \d+ \d{4} \d\d:\d\d:\d\d)\s*({host}[\w\-.]+)?"""
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
    """from\s+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[\w\-.]+))\/({src_port}\d+)""",
    """to\s+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[\w\-.]+))\/({dest_port}\d+)""",
    """({event_name}Invalid transport field) for protocol=({protocol}[^,]+)"""
]


}
```