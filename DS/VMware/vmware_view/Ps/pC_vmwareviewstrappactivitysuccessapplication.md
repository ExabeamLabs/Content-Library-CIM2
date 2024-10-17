#### Parser Content
```Java
{
Name = vmware-view-str-app-activity-success-application
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware View
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """View User""", """requested Application""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View User""",
    """View User\s+(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """requested Application\s+({object}\w+)""",
    """({operation}requested Application)""",
    """({app}View)"""
   ]


}
```