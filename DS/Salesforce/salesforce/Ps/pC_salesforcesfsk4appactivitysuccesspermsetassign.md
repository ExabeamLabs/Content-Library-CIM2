#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-permsetassign"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=PermSetAssign;"""
"""Sales Cloud"""
]
Fields = [
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""Action\\=({operation}[^;]+)"""
"""Display\\=({additional_info}.+?)\s*(\w+=|$)"""
"""Display\\=Permission set ({resource}.+?): assigned to user ({object}.+?)\s*(\w+=|$)"""
"""({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```