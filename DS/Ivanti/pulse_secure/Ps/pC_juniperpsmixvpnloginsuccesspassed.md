#### Parser Content
```Java
{
Name = "juniper-ps-mix-vpn-login-success-passed"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ PulseSecure:"""
  """ realm restrictions successfully passed"""
]
Fields = [
  """PulseSecure:\s+({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\d\d:\d\d:\d\d\s+\-\s+[^\s]+\s+\-\s+\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]"""
  """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)"""
  """passed for ({user}[^\s\\\/]+)[\\\/]({domain}[^\s\\\/]+)\s*$"""
  """PulseSecure:.*?\[(127\.0\.0\.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]\s+(({domain}[^\\\/]+)[\\\/])?({user}[^\s\\\/]+)[\\\/]?\((?:unknown|({realm}[^\)]+))?"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```