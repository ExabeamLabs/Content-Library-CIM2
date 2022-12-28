#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-sshsdisconnect
  ParserVersion = v1.0.0
  Conditions = [ """SSHS_DISCONNECT: """, """ SSH user """,""" disconnected from """ ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}SSHS_DISCONNECT)""",
    """IP: ({src_ip}[a-fA-F:\d\.]+)\)""",
    """SSH user (\(null\)|({user}[^\s]+))""",
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