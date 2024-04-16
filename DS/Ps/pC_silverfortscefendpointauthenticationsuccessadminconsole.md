#### Parser Content
```Java
{
Name = "silverfort-s-cef-endpoint-authentication-success-adminconsole"
Conditions = [
  """ CEF:"""
  """|Silverfort|Admin Console|"""
  """|MFA|MFA request|"""
  """SilverfortMfaResponse"""
  """ cs2=Allowed"""
]
ParserVersion = "v1.0.0"

auth0-authentication-template.Fields}[
    """"exa_regex=({operation_type}fcp)"""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "user->dest_user" 
}
```