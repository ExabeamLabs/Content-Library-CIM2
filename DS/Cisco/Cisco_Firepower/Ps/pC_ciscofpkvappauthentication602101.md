#### Parser Content
```Java
{
Name = cisco-fp-kv-app-authentication-602101
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
  """-602101"""
  """%FTD-""" 
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)"""
    """({event_name}PMTU-D packet 1406 bytes greater than effective mtu 1367)"""
    """%FTD-({priority}\d+)-({event_code}\d+)"""
    """dest_addr=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """src_addr=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """prot=({protocol}\w+)"""
  ]


}
```