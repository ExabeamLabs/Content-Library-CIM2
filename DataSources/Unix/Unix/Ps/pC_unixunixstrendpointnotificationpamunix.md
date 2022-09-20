#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-pamunix
  ParserVersion = v1.0.0
  Product = Unix
  Conditions = [ """ su """, """ pam_unix(su""" ]
  Fields = ${DLUnixParsersTemplates.unix-events.Fields}[
    """pam_unix\(su:\S*?:\s*({event_name}.+?)\s*$""",
  ]

unix-events = {
  Vendor = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """\[({src_ip}[a-fA-F\d.:]+)\]\[\d+\]\[\w+\]\[\]<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(\+|\-)\d\d:\d\d ({host}[\w.\-]+) ({event_code}\S+)""",
  
}
```