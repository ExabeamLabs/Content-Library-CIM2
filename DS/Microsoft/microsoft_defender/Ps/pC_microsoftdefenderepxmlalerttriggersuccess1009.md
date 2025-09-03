#### Parser Content
```Java
{
Name = microsoft-defenderep-xml-alert-trigger-success-1009
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>1009</EventID>""", """<Channel>Microsoft-Windows-Windows Defender/Operational</Channel>""", """<Data Name""", """>Microsoft Defender Antivirus</Data>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)'\/>""",
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Security UserID\\*=('|")({user_sid}[^'">]+)('|")\/>""",
    """<Data Name\\*=('|")Domain('|")>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")User('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>""",
    """<Data Name\\*=('|")Detection User('|")>(({domain}[^\<]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>""",
    """<Data Name\\*=('|")Severity ID('|")>({alert_severity}\d+)<\/Data>""",
    """<Data Name\\*=('|")Severity Name('|")>({alert_severity}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")Type Name('|")>({alert_type}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")Threat Name('|")>({alert_name}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")Threat ID('|")>({threat_id}\d+)<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```