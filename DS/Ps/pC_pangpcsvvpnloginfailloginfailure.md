#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-login-fail-loginfailure
  ParserVersion = v1.0.0
  Conditions = [
""",GLOBALPROTECT,""",
""",login,""",
""",failure,"""
  ]
  Fields = ${PaloAltoParsersTemplates.raw-pan-vpn-event.Fields}[
    """,({failure_reason}[^,]+),(|"[^"]*?"),failure,([^,]*?,)(|({failure_code}\d+)),"""
  ]


}
```