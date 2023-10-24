#### Parser Content
```Java
{
Name = "nexthink-nexthink-kv-alert-trigger-success-user"
Vendor = "Nexthink"
Product = "Nexthink Infinity"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" user ["""
""" User_type=""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+(\S+\s+){2}user \[.*?\] \[({alert_type}[^\[\]]+?)\] ({alert_name}.+?)\s+\["""
"""name="({user}[\w\.\-]{1,40}\$?)@({domain}[^@"]+)"""
"""display_name="({full_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```