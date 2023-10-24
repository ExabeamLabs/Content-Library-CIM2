#### Parser Content
```Java
{
Name = "unix-unix-str-group-member-add-success-usermod"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""to group"""
"""add"""
"""usermod"""
"""]:"""
]
Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(T|\s)\d\d:\d\d:\d\d(\.?\S+)? ({host}[\w.\-]+)(\s\S+)?\susermod\[""",
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\s*usermod"""
"""add \'({account_name}[^']+)\' to group \'({group_name}[^']+)\'"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```