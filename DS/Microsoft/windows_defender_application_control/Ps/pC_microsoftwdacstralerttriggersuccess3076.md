#### Parser Content
```Java
{
Name = microsoft-wdac-str-alert-trigger-success-3076
  Vendor = Microsoft
  Product = Windows Defender Application Control
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy" 
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-CodeIntegrity""", """3076""", """did not meet the""", """signing level requirements""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+MSWinEventLog""",
    """\s({time}\w{3}\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\d{4})""",
    """({event_code}3076)""",
    """Microsoft-Windows-CodeIntegrity\s+(N\/A|SYSTEM|LOCAL|NETWORK|({user}[\w\.\-]{1,40}\$?))\s"""
    """a process\s\(({process_path}({process_dir}[^"]*?)({process_name}[^\\\)]+?))\)\s""",
    """({alert_name}did not meet [^\(]+?)\s\(""",
    """({additional_info}Code Integrity [^<>]+\.)\s+({alert_id}\d+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```