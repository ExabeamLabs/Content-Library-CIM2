#### Parser Content
```Java
{
Name = "microsoft-defenderep-str-endpoint-scan-scanhasstarted"
  Product = Microsoft Defender
  Conditions = [ 
    """Microsoft-Windows-Windows Defender/Operational"""
    """Windows Defender scan has started"""
  ]
  Fields = ${WindowsParsersTemplates.windows-defender-1.Fields}[
    """Hostname":"({host}[^"]+?)"""",
    """"+host"+:"+({host}[^"]+)"+""",
    """AccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """({event_name}Windows Defender scan has started)"""
  ]
  ParserVersion = "v1.0.0"

windows-defender-1 = {
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
  Fields =[
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"EventReceivedTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"+@version"+:"+({version}[^"]+)"+""",
# system_info is removed
    """Severity":"({severity}[^"]+?)"""",
    """AccountType":"({user_type}[^"]+?)"""",
    """Message":"({additional_info}[^"]+?)\s*"""",
    """EventID":({event_code}\d+)""",
    """EventType":"({operation_type}[^"]+?)"""",
# src_name is removed
    
}
```