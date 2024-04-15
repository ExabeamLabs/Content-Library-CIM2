#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-dup-tcp"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = "Cisco Firepower"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""%FTD"""
"""Duplicate TCP SYN"""
  ]
  Fields = [
"""({host}[^\s]+)\s+:\s+%FTD"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
"""from ({src_interface}\w+):({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/*({src_port}\d*)"""
"""to ({dest_interface}\w+):({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/*(?:({dest_port}\d+))?"""
"""between ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? and ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""({event_name}Duplicate TCP SYN)"""
  ]


}
```