#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-success-statistics
  ParserVersion = v1.0.0
  Conditions = [ """PING_STATISTICS: """, """Ping statistics for """ ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}PING_STATISTICS)""",
    """({bytes_out}\d+) packet\(s\) transmitted""",
    """({bytes_in}\d+) packet\(s\) received""",
    """Ping statistics for ({src_ip}[a-fA-F:\d\.]+)\:"""
  ]

unix-events-1 = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w+\s+\d+ \d\d:\d\d:\d\d \d\d\d\d)""",
    """\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({host}[^\s]+)""",
  ]
  DupFields = [ "host->dest_host" 
}
```