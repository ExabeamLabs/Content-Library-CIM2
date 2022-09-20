#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-signature
  ParserVersion = "v1.0.0"
  Conditions = [ """ named[""", """request has invalid signature:""" ]
  Fields = ${NamedParserTemplates.named-dns-event.Fields} [
    """client ({dest_ip}[a-fA-F\d.:]+)\#({dest_port}\d+)""",
    """({event_name}request has invalid signature)""",
  ]

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