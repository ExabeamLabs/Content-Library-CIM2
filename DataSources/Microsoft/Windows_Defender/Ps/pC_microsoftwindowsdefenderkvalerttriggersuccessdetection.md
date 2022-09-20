#### Parser Content
```Java
{
Name = microsoft-windowsdefender-kv-alert-trigger-success-detection
  Vendor = Microsoft
  Product = Windows Defender
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """Microsoft Antimalware""", """Detection Origin""" ]
  Fields = [
    """,({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \d+),""",
    """(?:([^",]*,)){7}({src_host}[^,\.]+)""",
    """ComputerName =({src_host}[\w.\-]+)""",
    """\s+Name:\s+({alert_name}.+?)\s+ID:""",
    """\s+ID:\s+({alert_id}\d+)""",
    """\s+Severity:\s+({alert_severity}.+?)\s+Category""",
    """\s+Category:\s+({alert_type}.+?)\s+Path:""",
    """\s+Path:\s+({malware_url}.+?)(;|\s+Detection Origin)""",
    """\s+User:\s+({user}.+?)\s+Process Name:""",
    """C:\\Users\\({user}[^\\]+)"""
  ]


}
```