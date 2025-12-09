#### Parser Content
```Java
{
Name = "unix-unix-str-file-write-success-audit"
ParserVersion = "v1.0.0"
Vendor = "Unix"
Product = "Unix"
TimeFormat = [ "yyyy-MM-dd HH:mm:ss" , "epoch_sec", "MM/dd/yyyy HH:mm:ss.SSS" ]
Conditions = [
"""type="""
"""msg="""
"""audit"""
"""CREATE"""
]
Fields = [
    """name="({file_path}[^"]+)""""
    """name="({file_path}(({file_dir}[^\]]+)\/)?({file_name}[^"\\\/]+))"""
    """({dest_host}({host}[\w\-.]+))\s*(vcsa-audit|audispd:)"""
    """msg=audit\(({time}(\d{10})|\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\.\d+)"""
    """mode=({file_type}[^,]+),({file_permissions}[^\s]+)"""
]


}
```