#### Parser Content
```Java
{
Name = "unix-unix-kv-ssh-traffic-success-completedauth"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """SSH: Completed password Authentication. User logged in"""
    """SessionID="""
    """Listener="""
    """Client="""
    """<Host="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+) SSH:"""
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+),"""
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+),"""
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """Host=({dest_host}[^,]+)"""
    """SSH: ({event_name}[^<]+)\s+<"""
    """({event_code}SSH)"""
  ]
  ParserVersion = "v1.0.0"


}
```