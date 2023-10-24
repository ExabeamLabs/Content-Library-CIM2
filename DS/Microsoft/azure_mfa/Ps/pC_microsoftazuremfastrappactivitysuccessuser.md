#### Parser Content
```Java
{
Name = "microsoft-azuremfa-str-app-activity-success-user"
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""pfsvc: User"""
""" changed user """
""" value """
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+:\d+),({host}[^\s,]+),"pfsvc: User"""
"""pfsvc: User\s+"+(({email_address}[^"@]+@[^"]+)|(({domain}[^\\\s]+)\\)?({user}[\w\.\-]{1,40}\$?))"""
"""changed user "+({target}[^"]+)"+\s+({additional_info}value\s+({operation}[^=]+?)\s+from[^\.]+)\."""
"""changed user "+({target}[^"]+)"+\s+({additional_info}value\s+({operation}[^=]+?)\s+from "+[^"]+"+ to "+[^"]+"+)\."""
]
ParserVersion = "v1.0.0"


}
```