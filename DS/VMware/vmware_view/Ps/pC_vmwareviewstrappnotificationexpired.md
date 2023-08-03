#### Parser Content
```Java
{
Name = vmware-view-str-app-notification-expired
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware View
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """View""", """session on machine""", """has expired""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View""",
    """user\s+(({domain}[^\\\s]+)\\+)?(({email_address}[^@\s]+@[^\s]+)|({user}[\w\.\-]{1,40}\$?))\s+has expired""",
    """({app}View)""",
    """({operation}session)""",
    """({result}expired)"""
   ]


}
```