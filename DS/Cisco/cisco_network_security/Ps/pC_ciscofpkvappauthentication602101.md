#### Parser Content
```Java
{
Name = cisco-fp-kv-app-authentication-602101
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
  """-602101"""
  """%FTD-""" 
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)"""
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """({event_name}PMTU-D packet 1406 bytes greater than effective mtu 1367)"""
    """%FTD-({priority}\d+)-({event_code}\d+)"""
    """dest_addr=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """src_addr=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """prot=({protocol}\w+)"""
  ]


}
```