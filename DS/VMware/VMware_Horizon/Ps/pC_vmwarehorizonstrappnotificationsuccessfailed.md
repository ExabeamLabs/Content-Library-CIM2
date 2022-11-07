#### Parser Content
```Java
{
Name = vmware-horizon-str-app-notification-success-failed
  ParserVersion = "v1.0.0"
  Vendor = VMware 
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """ Backup of server """, """ failed with Error: """ ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """ Backup of server\s+({src_host}[\w\-.]+)""",
    """ failed with Error:\s*({failure_reason}.*?)\s+$""",
  ]


}
```