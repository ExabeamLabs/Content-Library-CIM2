#### Parser Content
```Java
{
Name = "questintrust-q-kv-endpoint-login-success-dnsrecord"
Vendor = "Quest InTrust"
Product = "Quest InTrust"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """Message=DNS record was"""
  """DNS Record Data:"""
]
Fields = [
  """ComputerName =({host}.+?)\s*Category"""
  """DNS Record Name[:\s]*({dest_host}[^\s.]+)"""
  """\s(New )?DNS Record Data[:\s]*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```