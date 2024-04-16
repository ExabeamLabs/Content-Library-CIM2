#### Parser Content
```Java
{
Name = microsoft-evapp-str-endpoint-notification-1530
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 1530 """, """ Windows detected your registry file is still in use by other applications or services""",""" MSWinEventLog """ ]
  Fields = [
    """({event_name}Windows detected your registry file is still in use by other applications or services)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}1530)"""
  ]


}
```