#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-dup-tcp"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""%FTD"""
"""Duplicate TCP SYN"""
  ]
  Fields = [
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
"""({protocol}[^\s]+)\s+SYN\s+from\s+({src_interface}.+?):(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))(\/({src_port}\d+)\s+)"""
"""to ({dest_interface}\w+):({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/*(?:({dest_port}\d+))?"""
"""between ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? and ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""({event_name}Duplicate TCP SYN)"""
  ]


}
```