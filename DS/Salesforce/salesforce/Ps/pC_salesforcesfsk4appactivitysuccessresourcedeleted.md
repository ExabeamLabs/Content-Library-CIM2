#### Parser Content
```Java
{
Name = "salesforce-sf-sk4-app-activity-success-resourcedeleted"
Vendor = "Salesforce"
Product = "Salesforce"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""IsDeleted\=true;"""
"""type\="""
"""LastModifiedBy.Name\="""
"""LastModifiedDate\="""
]
Fields = [
"""({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) \S+ """
"""LastModifiedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""LastModifiedBy\.Username\\=({email_address}[^@]+@({email_domain}[^\s;]+))"""
"""({operation}resource-deleted)"""
"""suser=(({email_address}[^@\s;=]+?@[^@\s;\.]+\.[^@\s;]+)|({user}[\w\.\-]{1,40}\$?))\s*(\w+=|$)"""
"""duser=(({dest_email_address}[^@",\s]+@[^@",\s\\]+)|({dest_user}[^@",\s]+))"""
"""fname=({object}.+?)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
"""({app}Sales Cloud)"""
"""Owner\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))"""
]
DupFields = [
"object->resource"
]
ParserVersion = "v1.0.0"


}
```