#### Parser Content
```Java
{
Name = vmware-horizon-str-app-authentication-view
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """ SSO """ ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """user\s+(({domain}[^\\\s]+)[\\\/]+)?({user}[^\\\s]+)""",
    """({operation}SSO)""",
  ]


}
```