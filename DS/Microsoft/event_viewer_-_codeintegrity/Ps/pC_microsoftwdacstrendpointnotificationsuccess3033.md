#### Parser Content
```Java
{
Name = microsoft-wdac-str-endpoint-notification-success-3033
  Vendor = Microsoft
  Product = Event Viewer - CodeIntegrity
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss yyyy"]
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-CodeIntegrity""", """3033""", """did not meet the""", """signing level requirements""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+MSWinEventLog""",
    """\s({time}\w{3}\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\d{4})""",
    """\s\w{3}\s+({time}\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\d{4})""",
    """({event_code}3033)""",
    """Microsoft-Windows-CodeIntegrity\s+(N\/A|SYSTEM|LOCAL|NETWORK|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """a process\s\(({process_path}({process_dir}[^"]*?)({process_name}[^\\\)]+?))\)\s""",
    """({additional_info}Code Integrity determined[^<>]+\.)\s+({alert_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```