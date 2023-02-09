#### Parser Content
```Java
{
Name = vmware-esxi-kv-app-notification-success-esxupdate
  ParserVersion = v1.0.0
  Conditions = [ """ esxupdate:""", """: """ ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """\sesxupdate:\s\d+:[^\n]+?(INFO|DEBUG):\s+({additional_info}[^\$]+?)\s*$"""
  ]

VMParserTemplates = {
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SS"
  Fields =[
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(.\d{1,3})?Z?)""",
  """T\d+:[^\s]+\s+({host}[\w.-]+)\s+({event_code}[^:]+?)(\[\d+\])?:\s+({additional_info}[^\$]+?)\s*$"""
  ]
 
}
```