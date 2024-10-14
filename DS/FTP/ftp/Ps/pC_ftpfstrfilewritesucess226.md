#### Parser Content
```Java
{
Name = ftp-f-str-file-write-sucess-226
  ParserVersion = v1.0.0
  Vendor = FTP
  Product = FTP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]created /""", """ - 226 """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) """,
    """({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]""",
    """({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]""",
    """(-|(({domain}\S+)[\/\\])?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\[\d+\]""",
    """\]created\s+(-|({file_name}\S+))\s""",
    """\]created\s+(-|({file_path}({file_dir}\/(\S+\/)?)({file_name}\S+)))\s""",
    """\]created\s+\/\S+\.({file_ext}[^\/\.\s]+)\s""",
    """\]created\s+(\S+\s+){2}({result}\d+)""",
    """\]created\s+(\S+\s+){4}({bytes}\d+)""",
  ]
  DupFields = [ "host->dest_host", "file_ext->host_file_ext" ]


}
```