#### Parser Content
```Java
{
Name = pingidentity-pi-json-endpoint-authentication-success-fail-idp
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """SSO_CALL":"""
  """Sensitive":"""
  """Status":"""
  """Transaction_ID":"""
]
Fields = [
  """"@timestamp"+:"+({time}[^"]+)"""
  """"+hostname"+:"+({host}[^"]+)"""
  """"+SAML_Subject"+:"+({email_address}[^"]+)"""
  """"+Sensitive"+:"+({src_ip}[^"]+)"""
  """"+SSO_CALL"+:"+({auth_method}[^"]+)"""
  """"+Application"+:"+\s(\s|({service_name}[^"]+))"""
  """"+Status"+:"+({result}[^"]+)"""
  """"+Sensitive_IAM_Server"+:"+({auth_server}[^"]+)"""
  """"+Protocol"+:"+({protocol}[^"]+)"""
  """"+Event"+:"+({operation}[^"]+)"""
  """"+ERROR"+:"+({failure_reason}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```