#### Parser Content
```Java
{
Name = microsoft-evsystem-str-ssl-start-fail-36874-1
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ 36874 """, """ connection request was received from a remote client application""" ,""" MSWinEventLog """]
  Fields = [
    """({event_code}36874)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_name}The SSL connection request has failed)""",
  ]
  DupFields = ["host->dest_host"]


}
```