#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-sshconnectionestablished"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
    """SSH: Connection established"""
    """<SessionID="""
    """Listener="""
    """Client="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+) SSH:"""
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)"""
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)"""
    """SSH: ({event_name}[^<]+)\s+<"""
    """SessionID=({session_id}\d+)"""
    """({event_code}SSH)"""
  ]
  ParserVersion = "v1.0.0"


}
```