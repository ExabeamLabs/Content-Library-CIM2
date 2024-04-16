#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-loggedoutfrom
  ParserVersion = v1.0.0
  Conditions = [ """logged out from """, """SHELL_LOGOUT: """ ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}SHELL_LOGOUT)""",
    """SHELL_LOGOUT: ({user}[\w\.\-]{1,40}\$?)""",
    """logged out from ({src_ip}[a-fA-F\d:\.]+)\.""",
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