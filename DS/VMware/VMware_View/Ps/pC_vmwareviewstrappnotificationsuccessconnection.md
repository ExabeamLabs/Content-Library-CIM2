#### Parser Content
```Java
{
Name = vmware-view-str-app-notification-success-connection
  ParserVersion = "v1.0.0"
  Conditions = [ """ View """, """The agent running on machine""", """has contacted the connection server""" ]
  Fields = ${VMWareParsersTemplates.vmware-view-events.Fields}[
    """({additional_info}contacted the [^"]+?)\s*$"""
   ]

vmware-view-events = {
    Vendor = VMware
    Product = VMware View
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View""",
      """({app}View)""",
      """(?:M|m)achine\s+({dest_host}[\w\-.]+)""",
      """(?:U|u)ser\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^@\s]+)|({user}[^\s]+))"""
    
}
```