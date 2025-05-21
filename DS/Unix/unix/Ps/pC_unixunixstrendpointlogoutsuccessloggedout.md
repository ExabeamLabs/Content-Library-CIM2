#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-logout-success-loggedout
  ParserVersion = v1.0.0
  Conditions = [ """logged out from """, """SSHS_LOG: """ ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}SSHS_LOG)""",
    """logged out from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """SSHS_LOG: User ({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
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