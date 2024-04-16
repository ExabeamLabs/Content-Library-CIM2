#### Parser Content
```Java
{
Name = "nexthink-nexthink-kv-alert-trigger-success-source"
Vendor = "Nexthink"
Product = "Nexthink Infinity"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
""" source ["""
""" computer_type="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+(\S+\s+){2}source \[.*?\] \[({alert_type}[^\[\]]+?)\] ({alert_name}.+?)\s+\["""
"""name="({src_host}[^"]+)"""
"""os_name="({os}[^"]+)"""
"""last_login_user="({user}[\w\.\-]{1,40}\$?)@({domain}[^@"]+)"""
]
ParserVersion = "v1.0.0"


}
```