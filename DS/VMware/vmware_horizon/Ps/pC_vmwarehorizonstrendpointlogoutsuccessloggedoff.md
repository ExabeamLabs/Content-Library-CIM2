#### Parser Content
```Java
{
Name = vmware-horizon-str-endpoint-logout-success-loggedoff
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """has logged off machine""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """User\s+(({domain}[^\\\s]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """ machine\s+({dest_host}[\w\-.]+)""",
  ]


}
```