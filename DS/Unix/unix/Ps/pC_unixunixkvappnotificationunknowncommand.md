#### Parser Content
```Java
{
Name = unix-unix-kv-app-notification-unknowncommand
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """FTPS: Unknown command""", """<SessionID=""", """Listener=""", """Client=""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[^\s]+) FTPS:""",
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)""",
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)""",
    """SessionID=({session_id}\d+)""",
    """FTPS: ({event_name}[^:]+)\s+""",
  ]


}
```