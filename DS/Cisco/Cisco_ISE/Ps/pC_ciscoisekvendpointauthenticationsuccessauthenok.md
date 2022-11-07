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
  """Caller-ID=(::ffff:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """User-Name =(?!host\/)(?:[a-f0-9]{12}|({user}[^,]+))"""
  """NAS-IP-Address=(::ffff:)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```