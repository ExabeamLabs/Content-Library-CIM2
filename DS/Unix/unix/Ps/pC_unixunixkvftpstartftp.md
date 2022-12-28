#### Parser Content
```Java
{
Name = unix-unix-kv-ftp-start-ftp
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """FTP: Connection established""", """<SessionID=""", """Listener=""", """Client=""", """><Command=""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[^\s]+) FTP:""",
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)""",
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)""",
    """FTP: ({event_name}[^<]+)\s+<""",
    """SessionID=({session_id}\d+)"""
  ]


}
```