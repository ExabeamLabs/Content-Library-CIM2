#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-login-success-connected
  ParserVersion = v1.0.0
  Conditions = [
""",GLOBALPROTECT,""",
""",connected,""",
""",success,"""
  ]
  Fields = ${PaloAltoParsersTemplates.raw-pan-vpn-event.Fields}[
    """,({app}GLOBALPROTECT),""",
    """({result}success|Success|SUCCESS)"""
  ]


}
```