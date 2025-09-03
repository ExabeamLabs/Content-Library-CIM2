#### Parser Content
```Java
{
Name = vmware-esxi-kv-app-notification-success-esxupdate
  ParserVersion = v1.0.0
  Conditions = [ """ esxupdate:""", """: """ ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """\sesxupdate:\s\d+:[^\n]+?(INFO|DEBUG):\s+({additional_info}[^\$]+?)\s*$"""
  ]


}
```