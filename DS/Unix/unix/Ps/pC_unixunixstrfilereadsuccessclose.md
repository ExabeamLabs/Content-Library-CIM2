#### Parser Content
```Java
{
Name = "unix-unix-str-file-read-success-close"
ParserVersion = "v1.0.0"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""sftp-server["""
""" close """
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+) sftp-server\["""
"""({operation}close) \"+({file_path}({file_dir}[^\"]*?[\\\/]+)?\s*({file_name}[^\"\\\/]*?(\.({file_ext}\w+))?))\"+"""
"""written ({bytes}\d+)"""
]
DupFields = [
"host->dest_host"
]


}
```