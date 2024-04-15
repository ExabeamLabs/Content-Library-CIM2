#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-changedpassword"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=changedpassword;"""
"""Sales Cloud"""
]
Fields = [
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""Action\\=({operation}[^;]+)"""
"""duser=({target}[^\\\s]+)"""
"""({app}Sales Cloud)"""
]
DupFields = [
"email_address->user"
]
ParserVersion = "v1.0.0"


}
```