#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-vsand
  ParserVersion = v1.0.0
  Product = VMware ESXi
  Conditions = [ """VSANMGMTSVC""", """ vsand[""" ]
   Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Initialized ObjectCache)"""
    ]


}
```