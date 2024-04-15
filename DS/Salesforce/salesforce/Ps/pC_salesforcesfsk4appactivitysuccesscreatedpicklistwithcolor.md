#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-createdpicklistwithcolor"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=createdPicklistWithColor;"""
"""Sales Cloud"""
]
Fields = [
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""Action\\=({operation}[^;]+)"""
"""Display\\=({additional_info}.+?)\s*(\w+=|$)"""
"""Display\\=Added value .*? to ({object}.+?) picklist"""
"""({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```