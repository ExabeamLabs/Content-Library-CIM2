#### Parser Content
```Java
{
Name = ftp-f-str-app-login-success-200
  ParserVersion = v1.0.0
  Vendor = FTP
  Product = FTP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]pass ******""", """ - 200 - - - """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) """,
    """({host}[\w\.-]+)\s+(\S+\s+){2}\[\d+\]""",
    """({src_ip}\S+)\s+(\S+\s+){2}\[\d+\]""",
    """(-|(({domain}\S+)[\/\\])?({user}[\w\.\-]{1,40}\$?))\s+\[\d+\]""",
    """\]pass\s+(\S+\s+){2}({result}\d+)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```