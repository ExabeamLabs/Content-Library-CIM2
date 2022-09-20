#### Parser Content
```Java
{
Name = cisco-fp-str-vpn-logout-success-602304
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """%FTD-6-602304""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\+\d\d:\d\d,({host}[^,]+),%FTD-""",
    """between ({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}) and ({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """(FTD-6-602304: IPSEC:\s({event_name}.+)SA)"""
    ]


}
```