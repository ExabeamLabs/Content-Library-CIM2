#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-805002"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """%FTD-6-805002"""
  ]
  Fields = [
    """({host}[^\s]+)\s+:\s+%FTD"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
    """from ({src_interface}\w+):({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/*({src_port}\d*)"""
    """to ({dest_interface}\w+):({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\/*(?:({dest_port}\d+))?"""
    """between ({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}) and ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """(FTD-6-805002:\s({event_name}.+connection))"""
  ]


}
```