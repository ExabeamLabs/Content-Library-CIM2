#### Parser Content
```Java
{
Name = vmware-esxi-str-endpoint-delete-removedvm
  ParserVersion = "v1.0.0"
  Product = "VMware ESXi"
  Conditions = [ """Fdm:""", """fdm[""",  """Removed VM """ ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Removed VM)"""
    ]


}
```