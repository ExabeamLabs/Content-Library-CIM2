#### Parser Content
```Java
{
Name = unix-unix-str-app-activity-sftp-server
  Vendor = Unix
  Product = Unix
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """sftp-server[""", """]: """ ]
  Fields = [
    """\ssftp-server\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """\d\d:\d\d:\d\d ({host}[^\s]+) sftp-server\[""",
    """\d\d:\d\d:\d\d\s({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*({host}[^\s]+)\s*sftp-server""",
  ]


}
```