#### Parser Content
```Java
{
Name = vmware-esxi-str-network-session-fail-iofiltervpd
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """iofiltervpd[""", """SSL Connection error""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """({event_name}SSL Connection error)"""
    ]


}
```