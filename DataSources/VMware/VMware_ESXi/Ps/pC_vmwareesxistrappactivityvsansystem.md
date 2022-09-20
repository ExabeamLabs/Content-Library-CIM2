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

VMParserTemplates = {
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SS"
  Fields =[
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d)""",
  """T\d+:[^\s]+\s+({host}[\w.-]+)\s+({event_code}[^:]+):\s+({additional_info}[^\$]+?)\s*$"""
  ]
 
}
```