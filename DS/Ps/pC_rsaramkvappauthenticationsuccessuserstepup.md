#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-success-userstepup
  Conditions = [ """ SINGLEPOINT """, """ USER_STEPUP_AUTHN """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}USER_STEPUP_AUTHN)""",
    """PROTECTED_RESOURCE="({resource}[^"]+)"""",
    """SENSITIVITY_LEVEL="({severity}[^"]+)"""",
# auth_scheme is removed
    """RESULT="({result}[^"]+)"""",
    """TENANT="({tenant_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```