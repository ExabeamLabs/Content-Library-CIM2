#### Parser Content
```Java
{
Name = cisco-fp-str-policy-modify-success-policies
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """@""", """, Policies > """ ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s+({host}[\w\-\.]+):\s*({process_name}[^:]+):\s*({user}[\w\.\-]{1,40}\$?)\@([\w\s]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),\s*({resource_path}[^,]+),\s*({additional_info}[^"]+)"""
  ]


}
```