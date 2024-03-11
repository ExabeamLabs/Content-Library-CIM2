#### Parser Content
```Java
{
Name = salesforce-sf-sk4-app-activity-success-resourcepropertyupdated
Vendor = Salesforce
Product = Salesforce
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """|resource-property-updated|"""
  """destinationServiceName =Sales Cloud"""
]
Fields = [
  """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) \S+ """
  """([^\|]*\|){5}({operation}[^\|]+)"""
  """\Wsuser=({user}.+?)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^@\s;]+?@[^@\s;]+)\s*(\w+=|$)"""
  """\Wfname=({object}.+?)\s+(\w+=|$)"""
  """\Wcs1=\{({new_value}[^\}]+)"""
  """\Wcs2=\{({old_value}[^\}]+)"""
  """\WdestinationServiceName =({app}.+?)\s*(\w+=|$)"""
]
DupFields = [
  "object->resource"
]
ParserVersion = "v1.0.0"


}
```