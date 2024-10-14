#### Parser Content
```Java
{
Name = "microsoft-azuremfa-str-app-activity-success-user"
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
"""pfsvc: User"""
""" changed user """
""" value """
]
Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
"""pfsvc:\s({additional_info}[^.$]+)."""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+:\d+),({host}[^\s,]+),"pfsvc: User"""
"""pfsvc: User\s+"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""changed user "+({target}[^"]+)"+\s+({additional_info}value\s+({operation}[^=]+?)\s+from[^\.]+)\."""
"""changed user "+({target}[^"]+)"+\s+({additional_info}value\s+({operation}[^=]+?)\s+from "+[^"]+"+ to "+(({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)|[^"]+)"+)\."""
]
ParserVersion = "v1.0.0"


}
```