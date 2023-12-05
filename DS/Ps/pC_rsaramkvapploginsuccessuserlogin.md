#### Parser Content
```Java
{
Name = rsa-ram-kv-app-login-success-userlogin
  Conditions = [ """ SINGLEPOINT """, """ USER_LOGIN """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """RESULT="({result}[^"]+)"""",
    """\]\s+({additional_info}User[^"]+?)\.*\s*$""",
# authn_source is removed
    """AUTHN_TYPE="({auth_method}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```