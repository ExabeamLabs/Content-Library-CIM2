#### Parser Content
```Java
{
Name = unix-unix-str-app-notification-success-stpnotifiedtc
  ParserVersion = v1.0.0
  Conditions = [ """STP_NOTIFIED_TC: """, """: Instance""" ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}STP_NOTIFIED_TC)""",
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