#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-createduser"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=createduser;"""
"""Sales Cloud"""
]
Fields = [
"""destinationServiceName =({host}.+?)\s*(\w+=|$)"""
"""destinationServiceName =({app}.+?)\s*(\w+=|$)"""
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""Display\\=({additional_info}Created new user ({object}.+?))\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```