#### Parser Content
```Java
{
Name = vmware-view-str-app-logout-success-loggedout
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware View
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """View User""", """ has logged out""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View User""",
    """View User\s+(({domain}[^\\\s]+)\\+)?({user}[^\s]+)""",
    """({app}View)"""
   ]


}
```