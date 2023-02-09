#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-notification-14554
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""14554""", """MSWinEventLog""", """Microsoft-Windows-DfsSvc"""]
  Fields = [
    """({host}[\w.-]+)\s+MSWinEventLog""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+14554""",
    """({event_code}14554)""",
    """({event_name}The DFS Namespaces service has successfully initialized the shared folder that hosts the namespace root)""",
# shared_folder is removed
  ]


}
```