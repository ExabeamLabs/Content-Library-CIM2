#### Parser Content
```Java
{
Name = rsa-ram-kv-app-logout-success-sessiontimeout
  Conditions = [ """ SINGLEPOINT """, """ USER_SESSION_REMOVED_TIMEOUT """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}USER_SESSION_REMOVED_TIMEOUT)""",
    """\]\s+({additional_info}[^"]+?)\.*\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```