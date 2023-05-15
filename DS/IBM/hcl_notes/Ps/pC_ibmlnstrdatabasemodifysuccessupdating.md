#### Parser Content
```Java
{
Name = ibm-ln-str-database-modify-success-updating
Vendor = IBM
Product = HCL Notes
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """  Updating '"""
  """' into database '"""
  """' from template '"""
]
Fields = [
  """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))"""
  """Updating .*? into database '({db_name}[^']+)"""
]
ParserVersion = "v1.0.0"


}
```