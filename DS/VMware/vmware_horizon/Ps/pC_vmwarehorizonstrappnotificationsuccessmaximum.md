#### Parser Content
```Java
{
Name = vmware-horizon-str-app-notification-success-maximum
  ParserVersion = "v1.0.0"
  Vendor = VMware 
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """ the maximum number """ ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """({event_name}View.*?)\s+$""",
  ]


}
```