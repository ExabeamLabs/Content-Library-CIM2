#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-resetpassword"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=resetpassword;"""
"""Sales Cloud"""
]
Fields = [
"""destinationServiceName =({host}[\w\-.]+?)\s*(\w+=|$)"""
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+));"""
"""Action\\=({operation}[^;]+)"""
"""duser=({object}[^\\\s]+)"""
"""\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
"""({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```