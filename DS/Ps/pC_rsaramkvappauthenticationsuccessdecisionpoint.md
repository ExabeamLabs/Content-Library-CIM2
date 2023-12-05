#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-success-decisionpoint
  Conditions = [ """ SINGLEPOINT """, """ USER_STEPUP_AUTH_DECISIONPOINT """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}USER_STEPUP_AUTH_DECISIONPOINT)""",
    """SENSITIVITY_LEVEL="({sensitivity_level}[^"]+)"""",
# auth_scheme is removed
  ]
  ParserVersion = "v1.0.0"


}
```