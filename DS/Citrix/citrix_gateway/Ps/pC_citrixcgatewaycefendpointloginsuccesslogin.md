#### Parser Content
```Java
{
Name = "citrix-cgateway-cef-endpoint-login-success-login"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "epoch"
Conditions = [
  """AAATM LOGIN"""
]
Fields = [
  """User\s+({domain}[^\\]+)\\+({user}[^\s]+)"""
  """Client_ip\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Vserver\s+(127.0.0.1|({host}[^:\s]+))"""
  """Browser_type\s+"+({user_agent}[^"]+)"""
  """SessionId:\s+({session_id}\d+)"""
  """\srt=({time}\d{13})"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```