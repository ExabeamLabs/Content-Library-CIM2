#### Parser Content
```Java
{
Name = vmware-view-str-endpoint-logout-success-disconnected
  ParserVersion = "v1.0.0"
  Conditions = [ """ View """ , """ has disconnected from machine """ ]
  Fields = ${VMWareParsersTemplates.vmware-view-events.Fields}[
    """({operation}disconnected from machine)"""
  ]

vmware-view-events = {
    Vendor = VMware
    Product = VMware View
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View""",
      """({app}View)""",
      """(?:M|m)achine\s+({dest_host}[\w\-.]+)""",
      """(?:U|u)ser\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    
}
```