#### Parser Content
```Java
{
Name = unix-unixnamed-str-network-notification-transferstarted
  Conditions = [ """ named[""", """Transfer started""" ]
  Fields = ${DLUnixParserTemplates.named-dns-event.Fields}[
    """zone ({dns_query}[^:\/]+)/({record_type}[^:/]+)""",
    """({event_name}Transfer started)""",
  ]
  ParserVersion = "v1.0.0"

named-dns-event = {
    Vendor = Unix
    Product = Unix Named
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """(::ffff:)?({host}[\w.\-]+)\s+named\[""",
      """\sfrom ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    
}
```