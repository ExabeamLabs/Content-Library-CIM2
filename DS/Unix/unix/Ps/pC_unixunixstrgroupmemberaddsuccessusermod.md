#### Parser Content
```Java
{
Name = "unix-unix-str-group-member-add-success-usermod"
Vendor = "Unix"
Product = "Unix"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
Conditions = [
"""to group"""
"""add"""
"""usermod"""
"""]:"""
]
Fields = [
"""({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({host}[\w.\-]+)\s*usermod"""
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)""",
"""(T|\s)\d\d:\d\d:\d\d(\.?\S+)? ({host}[\w.\-]+)(\s\S+)?\susermod\[""",
"""add \'({account_name}[^']+)\' to group \'({group_name}[^']+)\'"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```