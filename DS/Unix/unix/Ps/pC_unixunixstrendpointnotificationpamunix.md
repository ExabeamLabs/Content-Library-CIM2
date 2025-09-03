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
    """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\[\w+\]\[\]<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+)?(\+|\-)\d\d:\d\d ({host}[\w.\-]+) ({event_code}\S+)""",
  
}
```