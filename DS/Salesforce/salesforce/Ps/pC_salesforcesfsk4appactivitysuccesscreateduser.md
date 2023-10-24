#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-createduser"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=createduser;"""
"""type\=SetupAuditTrail;"""
"""Display\="""
]
Fields = [
"""destinationServiceName =({host}[\w\-.]+?)\s*(\w+=|$)"""
"""destinationServiceName =({app}.+?)\s*(\w+=|$)"""
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+));"""
"""Display\\=({additional_info}Created new user ({object}.+?))\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```