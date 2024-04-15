#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-resourcedeleted"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""|resource-deleted|"""
"""destinationServiceName =Sales Cloud"""
]
Fields = [
"""({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) \S+ """
"""LastModifiedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""LastModifiedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""({operation}resource-deleted)"""
"""suser=(({email_address}[^@\s;=]+?@[^@\s;\.]+\.[^@\s;]+)|({user}[^@\s=]+))\s*(\w+=|$)"""
"""duser=({dest_user}[^\\\s]+)"""
"""fname=({object}.+?)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
"""({app}Sales Cloud)"""
]
DupFields = [
"object->resource"
]
ParserVersion = "v1.0.0"


}
```