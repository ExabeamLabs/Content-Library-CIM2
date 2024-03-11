#### Parser Content
```Java
{
Name = pan-gp-cef-app-activity-success-globalprotect
  ParserVersion = "v1.0.0"
  Conditions = [ """,GLOBALPROTECT,"""]
  Fields = ${PaloAltoParsersTemplates.raw-pan-vpn-event.Fields}[
    """,({app}GLOBALPROTECT),""",
    """GLOBALPROTECT,([^,]*,){10}({src_host}[\w\-.]+),"""
    """GLOBALPROTECT,([^,]*,){19}"*({os}[^"]+)"""
  ]


}
```