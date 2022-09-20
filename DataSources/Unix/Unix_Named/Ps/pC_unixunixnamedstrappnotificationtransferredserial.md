#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-transferredserial
  Conditions = [ """ named[""", """transferred serial""" ]
  Fields = ${DLUnixParserTemplates.named-dns-event.Fields}[
    """zone ({dns_query}[^:\/]+)/({record_type}[^:/]+)""",
# serial is removed
  ]
  ParserVersion = "v1.0.0"

named-dns-event = {
    Vendor = Unix
    Product = Unix Named
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """(::ffff:)?({host}[\w.\-]+)\s+named\[""",
      """\sfrom ({dest_ip}[a-fA-F\d.:]+)""",
    
}
```