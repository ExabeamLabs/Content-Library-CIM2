#### Parser Content
```Java
{
Name = vmware-horizon-str-app-logout-success-loggedout
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """has logged out""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """User\s+(({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
  ]


}
```