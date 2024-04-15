#### Parser Content
```Java
{
Name = "shibboleth-s-str-endpoint-login-success-saml"
Vendor = "Shibboleth"
Product = "Shibboleth"
TimeFormat = "yyyyMMdd'T'HHmmssZ"
Conditions = [
  """shibboleth:"""
  """:SAML:"""
]
Fields = [
  """({time}\d{8}T\d{6}Z)\|(|({request_binding}[^\|]+))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|"""
  """({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\|\s*"""
  """\d{8}T\d{6}Z\|([^\|]*\|){7}(({email_address}(?!\d+)[^\@]+\@[^\|]+)|({user}(?!\d+)[^\|]+))\|"""
]
DupFields = [
  "request_binding->action"
]
ParserVersion = "v1.0.0"


}
```