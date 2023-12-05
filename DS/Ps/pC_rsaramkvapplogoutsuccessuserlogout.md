#### Parser Content
```Java
{
Name = rsa-ram-kv-app-logout-success-userlogout
  Conditions = [ """ SINGLEPOINT """, """ USER_LOGOUT """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """\]\s+({additional_info}[^"]+?)\.*\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```