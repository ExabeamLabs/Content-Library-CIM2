#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-loggedout
  ParserVersion = v1.0.0
  Conditions = [ """logged out from """, """SSHS_LOG: """ ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}SSHS_LOG)""",
    """logged out from ({src_ip}[a-fA-F:\d\.]+)""",
    """SSHS_LOG: User ({user}[^\s]+)""",
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