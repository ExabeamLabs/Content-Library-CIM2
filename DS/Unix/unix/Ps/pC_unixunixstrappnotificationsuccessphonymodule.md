#### Parser Content
```Java
{
Name = unix-unix-str-app-notification-success-phonymodule
  ParserVersion = v1.0.0
  Conditions = [ """PHONY_MODULE: """, """ -Slot=""" ]
  Fields = ${DLUnixParsersTemplates.unix-events-1.Fields}[
    """({event_name}PHONY_MODULE)""",
    """\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d\s+(\S+\s+){4}({additional_info}.+?)\s*$"""
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