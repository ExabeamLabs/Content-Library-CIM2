#### Parser Content
```Java
{
Name = microsoft-wdac-str-alert-trigger-success-3089
  Vendor = Microsoft
  Product = Windows Defender Application Control
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-CodeIntegrity""", """3089""", """Signature information for another event""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+MSWinEventLog""",
    """\s({time}\w{3}\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\d{4})""",
    """({event_code}3089)""",
    """Microsoft-Windows-CodeIntegrity\s+(N\/A|SYSTEM|LOCAL|NETWORK|({user}[\w\.\-]{1,40}\$?))\s""",
    """({additional_info}({alert_name}Signature information for another event)\.\s[^<>]+\.\s+({alert_id}\d+))"""
  ]
  DupFields = [ "host->dest_host" ]


}
```