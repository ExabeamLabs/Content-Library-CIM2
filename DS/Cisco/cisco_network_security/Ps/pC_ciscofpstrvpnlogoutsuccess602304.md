#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-logout-success-602304
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """%FTD-6-602304""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\+\d\d:\d\d,({host}[^,]+),%FTD-""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """between ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? and ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """(FTD-6-602304: IPSEC:\s({event_name}.+)SA)"""
    ]


}
```