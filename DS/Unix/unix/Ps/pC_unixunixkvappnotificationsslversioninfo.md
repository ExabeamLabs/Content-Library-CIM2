#### Parser Content
```Java
{
Name = unix-unix-kv-app-notification-sslversioninfo
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """FTP/SSL: SSL version info:""", """SessionID=""", """Listener=""", """Client=""", """User=""", """<Host=""", """><Command=""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[^\s]+) FTP\/SSL:""",
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)""",
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)""",
    """SessionID=({session_id}\d+)""",
    """FTP\/SSL: ({event_name}[^:]+):\s+\w+=""",
    """Host=({dest_host}[^,=]+?),\s+\w+=""",
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)><\w+="""
  ]


}
```