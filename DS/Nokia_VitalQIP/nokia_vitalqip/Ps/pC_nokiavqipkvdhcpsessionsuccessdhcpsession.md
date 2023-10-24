#### Parser Content
```Java
{
Name = "nokia-vqip-kv-dhcp-session-success-dhcpsession"
Vendor = "Nokia VitalQIP"
Product = "Nokia VitalQIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """qip"""
  """DHCP"""
  """ Host="""
  """ Domain="""
]
Fields = [
  """: Host=({dest_host}[^\s]+)"""
  """ IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Domain=({domain}[^\s]+)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```