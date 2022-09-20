#### Parser Content
```Java
{
Name = fileauditor-fa-kv-file-read-fail-readdeny
  ParserVersion = v1.0.0
  Vendor = FileAuditor
  Product = FileAuditor
  TimeFormat = "epoch_sec"
  Conditions = [ """[ FILE_ATTRIBUTES=""", """[ CREATION_TIME=""", """[ MESSAGE=Read Deny ]""" ]
  Fields = [
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d\d:\d\d\s+({host}[\w\-.]+)""",
    """\[ TIME_GENERATED=({time}\d{10})""",
    """\[ OLD_SHARE_PATH=({src_file_dir}[^\]]+\\+)?({src_file_name}[^\]\\\/]+?)\s*\]""",
    """\[ NEW_FILE_NAME=({file_path}({file_dir}[^\]]*?)[\\\/]*({file_name}[^\\\]]+?(\.({file_ext}[^\.\s\]]+))?))\s*\]""",
    """\[ CLIENT_IP=(::1|({src_ip}[A-Fa-f:\d.]+))""",
    """\[ CLIENT_HOST=({src_host}[\w\-.]+)""",
    """\[ MESSAGE=({access}.+?)\s*\]""",
    """\[ USERNAME=({user}[^\s\]]+)""",
  ]


}
```