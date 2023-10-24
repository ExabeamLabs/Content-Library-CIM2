#### Parser Content
```Java
{
Name = "namespacerdirectory-nrd-xml-user-password-modify-success-modifiedby"
Vendor = "Namespace rDirectory"
Product = "Namespace rDirectory"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""rdirectorySet password:"""
"""Modified by:"""
]
Fields = [
"""SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[^<]+)"""
"""Modified by:(({user}[\w\.\-]{1,40}\$?)|({full_name}[^",\(]+))\s+(\(.+?\))?\s+\(({domain}[^\/)]+)"""
"""Credentials:({account_domain}[^\\]+)\\+([^\s.]+\.)*({account}[^\s.]+)"""
"""password:({dest_user}.+?)\s+\(({dest_domain}[^\/)]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```