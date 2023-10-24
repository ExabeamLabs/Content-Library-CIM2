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

VMParserTemplates = {
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields =[
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((.\d{1,3})?Z?)""",
  """T\d+:[^\s]+\s+({host}[\w.-]+)\s+({event_code}[^:]+?)(\[\d+\])?:\s+({additional_info}[^\$]+?)\s*$"""
  ]
 
}
```