#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-success-userauthenticated
  Conditions = [ """ SINGLEPOINT """, """ USER_PROTECTED_APP_AUTHN """, """ RESULT="AUTHENTICATED"""" ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}USER_PROTECTED_APP_AUTHN)""",
    """RESULT="({result}[^"]+)"""",
    """TYPE="({auth_type}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```