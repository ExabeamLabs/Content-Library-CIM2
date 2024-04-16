#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-vmkwarning
  Conditions = [ """vmkwarning:""", """Invalid checksum""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Invalid checksum)"""
    ]
  ParserVersion = "v1.0.0"


}
```