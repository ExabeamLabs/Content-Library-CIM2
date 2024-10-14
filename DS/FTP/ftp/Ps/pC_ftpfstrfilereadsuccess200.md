#### Parser Content
```Java
{
Name = ftp-f-str-file-read-success-200
  ParserVersion = v1.0.0
  Vendor = FTP
  Product = FTP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]sent /""", """ - 200 """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) """,
    """({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]""",
    """({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]""",
    """(-|(({domain}\S+)[\/\\])?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\[\d+\]""",
    """\]sent\s+(-|({file_name}\S+))\s""",
    """\]sent\s+(-|({file_path}({file_dir}\/(\S+\/)?)({file_name}\S+)))\s""",
    """\]sent\s+\/\S+\.({file_ext}[^\/\.\s]+)\s""",
    """\]sent\s+(\S+\s+){2}({result}\d+)""",
    """\]sent\s+(\S+\s+){3}({bytes}\d+)""",
  ]
  DupFields = [ "host->dest_host", "file_ext->host_file_ext" ]


}
```