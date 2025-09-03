#### Parser Content
```Java
{
Name = unix-unix-str-app-notification-success-loginfo
  ParserVersion = v1.0.0
  Conditions = [ """Log Info""", """ -Slot=""" ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}Log Info)""",
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