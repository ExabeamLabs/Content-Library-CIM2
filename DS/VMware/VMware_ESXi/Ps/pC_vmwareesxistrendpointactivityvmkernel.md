#### Parser Content
```Java
{
Name = vmware-esxi-str-endpoint-activity-vmkernel
  ParserVersion = v1.0.0
  Conditions = [ """vmkernel:""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({event_name}Last path removed for TGT)"""
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