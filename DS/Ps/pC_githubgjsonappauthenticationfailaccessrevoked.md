#### Parser Content
```Java
{
Name = github-g-json-app-authentication-fail-accessrevoked
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"action":""", """"personal_access_token.access_revoked"""", """"operation_type":""", """"remove"""" ]
  DupFields = ["action->auth_type"]


}
```