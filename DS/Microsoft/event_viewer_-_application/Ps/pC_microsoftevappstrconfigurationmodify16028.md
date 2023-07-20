#### Parser Content
```Java
{
Name = microsoft-evapp-str-configuration-modify-16028
  Vendor = Microsoft
   Product = Event Viewer - Application
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  ParserVersion = "v1.0.0"
  Conditions = [  """ 16028 """, """ A forced configuration update """,""" MSWinEventLog """ ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}16028)""",
    """({event_name}A forced configuration update)"""
  ]


}
```