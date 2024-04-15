#### Parser Content
```Java
{
Name = "unix-unix-str-group-member-add-success-usermod"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""to group"""
"""add"""
"""usermod"""
"""]:"""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\s*usermod"""
"""add \'({account_name}[^']+)\' to group \'({group_name}[^']+)\'"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```