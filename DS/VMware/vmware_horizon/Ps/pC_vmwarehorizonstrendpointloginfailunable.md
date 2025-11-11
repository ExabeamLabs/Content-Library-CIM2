#### Parser Content
```Java
{
Name = vmware-horizon-str-endpoint-login-fail-unable
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """ Unable to launch from Pool """ ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """user\s+(({domain}[^\\\s:"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """({event_name}({operation}Unable to launch from Pool \w+).+?)[\s"]*$"""
    """ Unable to launch from Pool\s+({src_host}[\w\-.]+)""",
# machine is removed
# machine is removed
  ]


}
```