#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-deactivateduser"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=deactivateduser;"""
"""Sales Cloud"""
]
Fields = [
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""Action\\=({operation}[^;]+)"""
"""duser=({object}[^\\\s]+)"""
"""\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
"""({app}Sales Cloud)"""
]
DupFields = [
"email_address->user"
]
ParserVersion = "v1.0.0"


}
```