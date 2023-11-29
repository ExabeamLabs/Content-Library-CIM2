#### Parser Content
```Java
{
Name = microsoft-wdac-str-endpoint-notification-success-3099
  Vendor = Microsoft
  Product = Windows Defender Application Control
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss yyyy"]
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-CodeIntegrity""", """3099""", """Refreshed and activated Code Integrity policy""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+MSWinEventLog""",
    """\s({time}\w{3}\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\d{4})""",
    """\s\w{3}\s+({time}\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\d{4})""",
    """({event_code}3099)""",
    """Microsoft-Windows-CodeIntegrity\s+(N\/A|SYSTEM|LOCAL|NETWORK|({user}[\w\.\-]{1,40}\$?))\s""",
    """({additional_info}({event_name}Refreshed and activated Code Integrity policy)[^<>]+\.\s+Status\s({result_code}[^\s]+)\s+({alert_id}\d+))"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->dest_host" ]


}
```