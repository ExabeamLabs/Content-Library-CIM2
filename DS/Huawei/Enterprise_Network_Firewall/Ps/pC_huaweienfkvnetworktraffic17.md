#### Parser Content
```Java
{
Name = huawei-enf-kv-network-traffic-17
Vendor = "Huawei"
Product = "Enterprise Network Firewall"
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
  """source-ip=({src_ip}[^,]+)"""
  """source-port=({src_port}\d+)"""
  """destination-ip=({dest_ip}[^,]+)"""
  """destination-port=({dest_port}\d+)"""
  """rule-name=({rule}[^.]+)"""
]
ParserVersion = "v1.0.0"


}
```