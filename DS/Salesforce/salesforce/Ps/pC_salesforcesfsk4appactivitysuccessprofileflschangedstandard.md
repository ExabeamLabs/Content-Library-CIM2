#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-profileflschangedstandard"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""Action\=profileFlsChangedStandard"""
"""Sales Cloud"""
]
Fields = [
"""CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""CreatedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""suser=({user}.+?)\s+(\w+=|$)"""
"""suser=({email_address}[^@\s]+?@[^@\s]+)\s*(\w+=|$)"""
"""Action\\=({operation}[^;]+)"""
"""Display\\=({additional_info}.+?)\s*(\w+=|$)"""
"""Display\\=Change.*?:\s*({object}[^:]+?)\s+was changed"""
"""({app}Sales Cloud)"""
]
ParserVersion = "v1.0.0"


}
```