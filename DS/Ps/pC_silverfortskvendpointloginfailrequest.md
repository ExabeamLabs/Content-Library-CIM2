#### Parser Content
```Java
{
Name = "silverfort-s-kv-endpoint-login-fail-request"
Conditions = [
  """ CEF:"""
  """|Silverfort|Admin Console|"""
  """|MFA|MFA request|"""
  """SilverfortMfaResponse"""
  """ cs2=Denied"""
]
ParserVersion = "v1.0.0"

auth0-authentication-template.Fields}[
    """"exa_regex=({operation_type}fcp)"""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "user->dest_user" 
}
```