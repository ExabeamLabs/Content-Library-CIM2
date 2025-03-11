#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-notification-signature
  ParserVersion = "v1.0.0"
  Conditions = [ """ named[""", """request has invalid signature:""" ]
  Fields = ${NamedParserTemplates.named-dns-event-1.Fields} [
    """client ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({dest_port}\d+)""",
    """({event_name}request has invalid signature)""",
    """({time}\w+\s\d+\s\d+:\d+:\d+)"""
  ]

named-dns-event-1 = {
    Vendor = Unix
    Product = Unix Named
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """(::ffff:)?({host}[\w.\-]+)\s+named\[""",
      """\sfrom ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    
}
```