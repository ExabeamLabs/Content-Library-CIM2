#### Parser Content
```Java
{
Name = vmware-view-str-endpoint-authentication-success-application
  ParserVersion = "v1.0.0"
  Conditions = [ """ View """, """ requested an application session """ ]
  Fields = ${VMWareParsersTemplates.vmware-view-events.Fields}[
  """({additional_info}View [^"]+?)\s*$""",
    """({operation}requested an application session)"""
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