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
"""CreatedBy\.Username\\=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+));"""
"""Action\\=({operation}[^;]+)"""
"""duser=({target}[^\\\s]+)"""
"""({app}Sales Cloud)"""
"""CreatedBy\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))"""
]
ParserVersion = "v1.0.0"


}
```