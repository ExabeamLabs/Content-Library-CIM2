#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-vsansystem
  ParserVersion = v1.0.0
  Product = VMware ESXi
  Conditions = [ """vsansystem:""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Invalid soap session cookie id|ObjLibPluginInit)"""
    ]


}
```