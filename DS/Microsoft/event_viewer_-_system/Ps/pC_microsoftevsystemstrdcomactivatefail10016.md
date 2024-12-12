#### Parser Content
```Java
{
Name = microsoft-evsystem-str-dcom-activate-fail-10016
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 10016 """, """ This security permission can be modified using the Component Services administrative tool.""",""" MSWinEventLog """ ]
  Fields = [
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}18453)""",
    """user (N\/A|(({domain}[^\\']+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+SID\s""",
    """\WCLSID\s*\{({cls_id}[^}\s]+)\}\s*""",
    """APPID\s+\{({app_id}[^\}]+)\}\s+""",
    """({event_name}This security permission can be modified using the Component Services administrative tool)"""
  ]


}
```