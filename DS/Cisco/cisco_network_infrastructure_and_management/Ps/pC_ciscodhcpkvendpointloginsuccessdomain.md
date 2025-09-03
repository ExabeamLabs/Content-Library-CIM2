#### Parser Content
```Java
{
Name = cisco-dhcp-kv-endpoint-login-success-domain
Vendor = "Cisco"
Product = "Cisco Network Infrastructure and Management"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """ hn=""""
  """ ip=""""
  """ hn16=""""
]
Fields = [
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
  """\shn="({dest_host}[^"]+?)""""
  """\sip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```