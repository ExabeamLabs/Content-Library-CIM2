#### Parser Content
```Java
{
Name = "unix-unix-str-group-member-remove-success-removed"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """removed by""", """from group""", """user""", """gpasswd""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\sgpasswd"""
"""user ({account_name}.+?) removed by ({user}[\w\.\-\!\#\^\~]{1,40}\$?) from group ({group_name}.+?)\s*$"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```