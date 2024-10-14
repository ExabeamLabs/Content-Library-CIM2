#### Parser Content
```Java
{
Name = "kemp-loadmaster-str-endpoint-login-success-loggedon"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ l7log:"""
  """ logged on from """
]
Fields = [
  """\s({host}[\w\.\-]+)\s+\S+\s+\S+\s+l7log:"""
  """l7log:\s+(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s:]+))"""
  """from\s+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s:]+))"""
  """\sUser\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+logged"""
]
ParserVersion = "v1.0.0"


}
```