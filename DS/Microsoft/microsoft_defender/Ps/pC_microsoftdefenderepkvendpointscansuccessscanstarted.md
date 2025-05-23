#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-endpoint-scan-success-scanstarted
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender"
  Conditions = [ """Microsoft-Windows-Windows Defender/Operational""", """Windows Defender Antivirus scan has started"""]
  Fields = ${WindowsParsersTemplates.windows-defender-1.Fields}[
    """({event_name}Windows Defender Antivirus scan has started)""",
    """User:\s*(NT AUTHORITY|({domain}[^\\]+))[\\]+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    ]

windows-defender-1 = {
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
  Fields =[
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"EventReceivedTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """Hostname":"({host}[^"]+?)"""",
    """"+host"+:"+({host}[^"]+)"+""",
    """"+@version"+:"+({version}[^"]+)"+""",
# system_info is removed
    """Severity":"({severity}[^"]+?)"""",
    """AccountType":"({user_type}[^"]+?)"""",
    """Message":"({additional_info}[^"]+?)\s*"""",
    """AccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """EventID":({event_code}\d+)""",
    """EventType":"({operation_type}[^"]+?)"""",
# src_name is removed
    
}
```