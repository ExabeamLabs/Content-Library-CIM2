#### Parser Content
```Java
{
Name = ftp-f-str-file-delete-success-250
  ParserVersion = v1.0.0
  Vendor = FTP
  Product = FTP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]dele """, """ - 250 - - - """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) """,
    """({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]""",
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+(\S+\s+){2}\[\d+\]""",
    """(-|(({domain}\S+)[\/\\])?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\[\d+\]""",
    """\]dele\s+(-|({file_name}\S+))\s""",
    """\]dele\s+(-|({file_path}({file_dir}\/(\S+\/)?)({file_name}\S+)))\s""",
    """\]dele\s+\/\S+\.({file_ext}[^\/\.\s]+)\s""",
    """\]dele\s+(\S+\s+){2}({result}\d+)""",
  ]


}
```