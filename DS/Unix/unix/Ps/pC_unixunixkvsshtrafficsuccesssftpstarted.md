#### Parser Content
```Java
{
Name = "unix-unix-kv-ssh-traffic-success-sftpstarted"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """channel: SFTP subsystem started in channel"""
    """c_Window: """
    """c_MaxPacket: """
    """s_Window: """
    """s_MaxPacket: """
  ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+) channel:"""
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+),"""
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+),"""
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """Host=({dest_host}[^,]+)"""
    """channel: ({event_name}[^:]+?)\s+\w+:"""
  ]
  ParserVersion = "v1.0.0"


}
```