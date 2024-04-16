#### Parser Content
```Java
{
Name = "zeek-z-json-endpoint-login-fail-resumed"
Product = "Zeek"
Conditions = [
  """server_name":"""
  """"resumed":"""
  """"id.resp_h":"""
  """"established":false"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

auth0-authentication-template.Fields}[
    """"exa_regex=({operation_type}fcp)"""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "user->dest_user" 
}
```