#### Parser Content
```Java
{
Name = unix-unix-kv-ftp-close-success-connectionaborted
  ParserVersion = v1.0.0
  Conditions = [ """FTPS: SendResponse:""", """connection was aborted""", """><Command=""", """<SessionID=""", """Listener=""", """Client=""" ]

unix-logout = {
    Vendor = Unix
    Product = Unix
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\d\d:\d\d:\d\d ({host}[^\s]+) [\w\/]+:""",
      """Listener=({dest_ip}[\da-fA-F:\.]+):({dest_port}\d+)""",
      """Client=({src_ip}[\da-fA-F:\.]+):({src_port}\d+)""",
      """User=({user}[\w\.\-\!\#\^\~]{1,40}\$?)>(<\w+=)?""",
      """Host=({dest_host}[^,=]+?),\s+\w+=""",
      """SessionID=({session_id}\d+)""",
      """(FTPS?(\/SSL)?|SSH): ({event_name}[^<:]+)(:\s+({additional_info}[^<]+?))?\s+<""",
      """({event_code}SSH)"""
    
}
```