#### Parser Content
```Java
{
Name = unix-unix-str-app-activity-sftp
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """SFTP: """, """SessionID=""", """Listener=""", """Client=""", """<Host=""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+) SFTP:""",
    """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)""",
    """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)""",
    """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)><\w+=""",
    """Host=({dest_host}[^,=]+?),\s+\w+=""",
    """({app}SFTP)""",
    """SFTP: ({additional_info}[^<]+?)\s+<Host""",
    """SFTP: ({operation}[^\s]+)\s+'({object}[^']+)'"""
  ]
  ParserVersion = "v1.0.0"


}
```