#### Parser Content
```Java
{
Name = "citrix-cgateway-cef-endpoint-login-success-login"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = ["epoch", "MM/dd/yyyy:HH:mm:ss"]
Conditions = [
  """AAATM LOGIN"""
]
Fields = [
  """\s({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+"""
  """User\s+({domain}[^\\]+)\\+(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """Client_ip\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Vserver\s+(127.0.0.1|({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+)))"""
  """Browser_type\s+"+({user_agent}[^"]+)"""
  """SessionId:\s+({session_id}\d+)"""
  """\srt=({time}\d{13})"""
]
ParserVersion = "v1.0.0"


}
```