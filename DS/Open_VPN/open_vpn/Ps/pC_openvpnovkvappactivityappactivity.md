#### Parser Content
```Java
{
Name = "openvpn-ov-kv-app-activity-appactivity"
Vendor = "Open VPN"
Product = "Open VPN"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """, mapping:"""
  """, request size:"""
]
Fields = [
  """timestamp:\s*\[({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+)"""
  """Cmd\\*=({operation}[^\s&"]+)"""
  """User\\*=({user}[^\s&%"]+)"""
  """DeviceType\\*=({src_host}[\w\-.]+)"""
  """request size:\s*({bytes}\d+)"""
  """mapping:\s*({app}.+?)\s*,"""
  """ip:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({additional_info}[^\s,]+?)\s*,\s*status:"""
  """status:\s*({result}\d+)"""
]
ParserVersion = "v1.0.0"


}
```