#### Parser Content
```Java
{
Name = xps-s-kv-printer-activity-success-set
Vendor = "XPS"
Product = "XPS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """printer="""
  """type="""
  """operation="""
  """attributes="""
]
Fields = [
  """printer=({printer_name}[^\s]+)"""
  """type=({object}[^\s]+)\s*\W"""
  """attributes=({bytes}\d+)\s*"""
  """operation=({operation}[^\s]+)\s*\W+"""
]
DupFields = [
  "printer_name->dest_host"
]
ParserVersion = "v1.0.0"


}
```