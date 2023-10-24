#### Parser Content
```Java
{
Name = vmware-horizon-kv-app-activity-success-module
  ParserVersion = "v1.0.0"
  Vendor = VMware 
  Product = VMware Horizon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ View """ , """ Severity""" , """ Module""" , """EventType=""" ]
  Fields = [
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)""",
    """({app}View)""",
    """EventType="*({event_name}[^"]+)"""
    """UserDisplayName ="*(({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
    """SessionType="*({operation}[^"]+)""",
    """UserSID="*({user_sid}[^"]+)""",
    """Module="*({resource}[^"]+)""",
    """ApplicationId="*({object}[^"]+)"""
  ]


}
```