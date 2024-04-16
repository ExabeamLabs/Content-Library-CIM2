#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-info
  ParserVersion = v1.0.0
  Product = VMware ESXi
  Conditions = [ """hostd-probe:""", """info """ ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """sub=Default\]\s+({event_name}[^"\$]+?)\s*($|")"""
    ]


}
```