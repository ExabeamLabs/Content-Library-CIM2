#### Parser Content
```Java
{
Name = unix-unixnamed-str-network-notification-notifyforzone
  Conditions = [ """ named[""", """received notify for zone""" ]
  Fields = ${DLUnixParserTemplates.named-dns-event.Fields}[
    """client\s+({src_ip}[a-fA-F\d.:]+)""",
    """({event_name}received notify for zone) '({dns_query}[^']+)"""
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