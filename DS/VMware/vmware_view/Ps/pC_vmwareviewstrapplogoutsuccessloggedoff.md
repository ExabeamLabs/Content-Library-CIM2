#### Parser Content
```Java
{
Name = vmware-view-str-app-logout-success-loggedoff
  ParserVersion = "v1.0.0"
  Conditions = [ """ View """ , """ has logged off from """ ]
  Fields = ${VMWareParsersTemplates.vmware-view-events.Fields}[
    """({additional_info}User\s[^"]+?)\s*$""",
    """({operation}logged off)"""
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