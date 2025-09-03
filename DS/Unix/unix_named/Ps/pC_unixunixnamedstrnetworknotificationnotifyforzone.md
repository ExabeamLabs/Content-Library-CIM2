#### Parser Content
```Java
{
Name = unix-unixnamed-str-network-notification-notifyforzone
  Conditions = [ """ named[""", """received notify for zone""" ]
  Fields = ${DLUnixParserTemplates.named-dns-event.Fields}[
    """client\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}received notify for zone) '({dns_query}[^']+)"""
  ]
  ParserVersion = "v1.0.0"

named-dns-event = {
    Vendor = Unix
    Product = Unix Named
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
    Fields = [
      """({time}\w+\s\d+\s\d+:\d+:\d+)(\s*(::ffff:)?({host}[\w.\-]+)\s+named\[)?""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\sfrom ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    
}
```