#### Parser Content
```Java
{
Name = unix-unix-kv-network-close-stopssl
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """FTPS: StopSSL:""", """<SessionID=""", """Listener=""", """Client=""", """><Command=""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)? ({host}[^\s]+) FTPS:""",
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)""",
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)""",
    """SessionID=({session_id}\d+)""",
    """FTPS: ({event_name}[^:]+): ({additional_info}[^<]+)\s+<""",
  ]


}
```