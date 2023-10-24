#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-createdrole"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=createdrole"""
"""Sales Cloud"""
]
Fields = [
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""suser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s*(\w+=|$)"""
"""Action\\=({operation}[^;]+)"""
"""Display\\=({additional_info}.+?)\s*(\w+=|$)"""
"""Display\\=Created new role Field Service\s*\-\s*({object}.+?)\s+(\w+=|$)"""
"""({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```