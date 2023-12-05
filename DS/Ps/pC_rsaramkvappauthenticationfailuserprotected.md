#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-fail-userprotected
  Conditions = [ """ SINGLEPOINT """, """ USER_PROTECTED_APP_AUTHN """, """ RESULT="NOT_AUTHENTICATED"""" ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}USER_PROTECTED_APP_AUTHN)""",
    """RESULT="({result}[^"]+)"""",
    """TYPE="({auth_method}[^"]+)"""",
    """REASON="({failure_reason}[^"]+)"""",
    """\]\s+({failure_reason}[^"]+?)\.*\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```