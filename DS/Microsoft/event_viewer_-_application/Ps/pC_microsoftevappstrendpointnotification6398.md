#### Parser Content
```Java
{
Name = microsoft-evapp-str-endpoint-notification-6398
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 6398 """, """ The Execute method of job definition """,""" MSWinEventLog """ ]
  Fields = [
     """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
     """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
     """({event_code}6398)""",
	 """({event_name}The Execute method of job definition)""",

  ]


}
```