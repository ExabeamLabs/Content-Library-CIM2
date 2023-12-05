#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-success-userauthenticated-1
  Conditions = [ """ SINGLEPOINT """, """ USER_STEPUP_AUTHN """, """ RESULT="AUTHENTICATED"""" ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """PROTECTED_RESOURCE="({resource}[^"]+)"""",
    """SENSITIVITY_LEVEL="({sensitivity_level}[^"]+)"""",
# auth_scheme is removed
    """RESULT="({result}[^"]+)"""",
    """TENANT="({tenant}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```