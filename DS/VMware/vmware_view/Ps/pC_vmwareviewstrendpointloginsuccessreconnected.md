#### Parser Content
```Java
{
Name = vmware-view-str-endpoint-login-success-reconnected
  ParserVersion = "v1.0.0"
  Conditions = [ """ View """, """ has reconnected to machine """ ]
  Fields = ${VMWareParsersTemplates.vmware-view-events.Fields}[
    """({additional_info}reconnected to [^"]+?)\s*$""",
    """({operation}reconnected to machine)"""
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