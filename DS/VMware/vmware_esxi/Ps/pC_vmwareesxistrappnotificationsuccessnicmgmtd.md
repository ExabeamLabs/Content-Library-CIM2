#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-success-nicmgmtd
  ParserVersion = v1.0.0
  Conditions = [ """ nicmgmtd[""", """]: """ ]

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