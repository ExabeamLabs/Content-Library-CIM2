#### Parser Content
```Java
{
Name = pingidentity-pi-json-endpoint-authentication-success-fail-idp
Vendor = Ping Identity
Product = Ping Identity
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
  """SSO_CALL":"""
  """Sensitive":"""
  """Status":"""
  """Transaction_ID":"""
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time"""
  """exa_json_path=$.hostname,exa_field_name=host"""
  """exa_json_path=$.SAML_Subject,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_json_path=$.Sensitive,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.SSO_CALL,exa_field_name=auth_method"""
  """exa_json_path=$.Application,exa_field_name=time"""
  """exa_json_path=$.Status,exa_field_name=result"""
  """exa_json_path=$.Sensitive_IAM_Server,exa_field_name=auth_server"""
  """exa_json_path=$.Protocol,exa_field_name=protocol"""
  """exa_json_path=$.Event,exa_field_name=operation"""
  """exa_json_path=$.ERROR,exa_field_name=failure_reason"""
]
ParserVersion = "v1.0.0"


}
```