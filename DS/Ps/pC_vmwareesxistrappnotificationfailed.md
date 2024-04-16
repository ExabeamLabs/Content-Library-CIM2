#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-failed
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """vsfwd:""", """[ERROR] failed""",  """invalid argument""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """({event_name}failed to create rule)"""
    ]
  ParserVersion = "v1.0.0"


}
```