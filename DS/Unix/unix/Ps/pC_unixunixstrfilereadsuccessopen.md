#### Parser Content
```Java
{
Name = "unix-unix-str-file-read-success-open"
ParserVersion = "v1.0.0"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""sftp-server["""
""" open """
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+) sftp-server\["""
"""({operation}open) \"+({file_path}({file_dir}[^\"]*?[\\\/]+)?\s*({file_name}[^\"\\\/]*?(\.({file_ext}\w+))?))\"+"""
"""flags ({access}.+?) mode"""
]
DupFields = [
"host->dest_host"
]


}
```