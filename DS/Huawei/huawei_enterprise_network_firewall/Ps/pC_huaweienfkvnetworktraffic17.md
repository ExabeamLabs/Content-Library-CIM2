#### Parser Content
```Java
{
Name = huawei-enf-kv-network-traffic-17
Vendor = "Huawei"
Product = "Huawei Enterprise Network Firewall"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """rule-name="""
  """vsys="""
  """destination-ip"""
  """POLICY/"""
  """/POLICY"""
]
Fields = [
  """time=({time}\d\d\d\d\/\d+\/\d+\s*\d\d:\d\d:\d\d)"""
  """\s({host}[^\s]+)\s%"""
  """%*\d*POLICY\/\d\/POLICY({action}\w+)"""
  """protocol=({protocol}[^,]+)"""
  """source-ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """source-port=({src_port}\d+)"""
  """destination-ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """destination-port=({dest_port}\d+)"""
  """rule-name=({rule}[^.]+)"""
]
ParserVersion = "v1.0.0"


}
```