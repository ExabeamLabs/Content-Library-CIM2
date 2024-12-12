#### Parser Content
```Java
{
Name = "microsoft-evfsscp-str-endpoint-notification-success-shadowcopy"
Vendor = "Microsoft"
Product = "Event Viewer - FileShareShadowCopyProvider"
Conditions = [
"""MSWinEventLog"""
"""Microsoft-Windows-FileShareShadowCopyProvider"""
"""Microsoft File Share Shadow Copy Provider"""
]
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Fields = [
    """\s({time}[a-zA-Z]{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """({time}\d{1,4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """Microsoft-Windows-FileShareShadowCopyProvider\/[^\s]+\s+\-?\s*({event_code}\d+)\s+\w{3}\s\w{3}"""
    """({host}[\w\-\.]+)\s+None"""
    """\s({src_ip}((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?\s+[^\s]+\s+\-?\s*MSWinEventLog"""
    """({log_name}MSWinEventLog)"""
    """None\s+({event_name}Microsoft File Share Shadow Copy Provider)"""
  ]
ParserVersion = "v1.0.0"


}
```