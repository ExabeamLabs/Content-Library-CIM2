#### Parser Content
```Java
{
Name = "unix-unix-str-file-write-success"
ParserVersion = "v1.0.0"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""sftp-server["""
""" rename """
]
Fields = [
  """\d\d:\d\d:\d\d ({host}[^\s]+) sftp-server\["""
  """({operation}rename)"""
  """old "+({src_file_dir}(\/[^\/]+)*\/)?({src_file_name}[^\/"]+)"+\snew\s"+({file_path}({file_dir}[^"]*?[\\\/]+)?\s*({file_name}[^"\\\/]*?(\.({file_ext}\w+))?))"+"""
  """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
]
DupFields = [
"host->dest_host"
]


}
```