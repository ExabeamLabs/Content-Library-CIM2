#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-auth
  ParserVersion = v1.0.0
  Product = Unix
  Conditions = [ """ su """, """ auth.notice]""" ]
  Fields = ${DLUnixParsersTemplates.unix-events.Fields}[
    """'({command}su ({user}[^']+))'""",
  ]

unix-events = {
  Vendor = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[\w+\]\[\]<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(\+|\-)\d\d:\d\d ({host}[\w.\-]+) ({event_code}\S+)""",
  
}
```