#### Parser Content
```Java
{
Name = vmware-esxi-str-app-notification-failed
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """vsfwd:""", """[ERROR] failed""",  """invalid argument""" ]
  Fields = ${VMDLParsersTemplates.VMParserTemplates.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """({event_name}failed to create rule)"""
    ]
  ParserVersion = "v1.0.0"

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