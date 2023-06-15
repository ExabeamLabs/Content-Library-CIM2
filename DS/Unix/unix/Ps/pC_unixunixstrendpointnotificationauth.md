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
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[\w+\]\[\]<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(\+|\-)\d\d:\d\d ({host}[\w.\-]+) ({event_code}\S+)""",
  
}
```