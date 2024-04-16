#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-success-logonsuccess"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """FTP/SSL: logon success"""
    """SessionID="""
    """Listener="""
    """Client="""
    """User="""
    """<Host="""
    """><Command="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+) FTP\/SSL:"""
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)"""
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)"""
    """FTP\/SSL: ({event_name}[^\(]+)\s\("""
    """SessionID=({session_id}\d+)"""
    """Host=({dest_host}[^,=]+?),\s+\w+="""
    """User=({user}[\w\.\-]{1,40}\$?)><\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```