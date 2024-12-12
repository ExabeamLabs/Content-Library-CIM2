#### Parser Content
```Java
{
Name = "microsoft-evsystem-str-endpoint-notification-success-mswineventlog"
Vendor = "Microsoft"
Product = "Event Viewer - System"
Conditions = [
""" - MSWinEventLog -"""
"""Snare_Enterprise_Agent_for_Windows"""
]
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Fields = [
    """\s({time}[a-zA-Z]{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """({time}\d{1,4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """[^\s]+\s+\-?\s*({event_code}\d+)\s+\w{3}\s\w{3}"""
    """({host}[\w\-\.]+)\s+None"""
    """\s({src_ip}((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?\s+[^\s]+\s+\-?\s*MSWinEventLog"""
    """({log_name}MSWinEventLog)"""
  ]
ParserVersion = "v1.0.0"


}
```