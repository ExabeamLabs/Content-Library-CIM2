#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-authentication-success-authenok
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Message-Type=Authen OK"""
  """_PassedAuth"""
]
Fields = [
  """Caller-ID=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """User-Name =(?!host\/)(?:[a-f0-9]{12}|({user}[^,]+))"""
  """NAS-IP-Address=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```