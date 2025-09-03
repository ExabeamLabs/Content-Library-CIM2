#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-time-modify-success-stratumchanged
  ParserVersion = v1.0.0
  Conditions = [ """NTP_STRATUM_CHANGE: """, """System stratum changed""" ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}NTP_STRATUM_CHANGE)""",
    """NTP_STRATUM_CHANGE: ({additional_info}[^.]+)"""
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