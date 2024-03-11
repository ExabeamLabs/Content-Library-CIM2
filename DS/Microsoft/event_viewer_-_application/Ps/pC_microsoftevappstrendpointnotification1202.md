#### Parser Content
```Java
{
Name = microsoft-evapp-str-endpoint-notification-1202
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """1202""", """Security policies were propagated with warning""" ]
  Fields = [
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}1202)""",
    """({event_name}Security policies were propagated with warning)\.\s*({result_code}[\w]+)\s:"""
  ]


}
```