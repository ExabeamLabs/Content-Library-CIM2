#### Parser Content
```Java
{
Name = "unix-unix-str-group-member-add-success-gpasswd"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """to group""", """added by""", """gpasswd""" ]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w.\-]+)\sgpasswd"""
"""user ({account_name}.+?) added by ({user}[\w\.\-]{1,40}\$?) to group ({group_name}.+?)\s*$"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```