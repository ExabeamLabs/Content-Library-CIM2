#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-app-notification-scanfinished
  Product = Microsoft Defender for Endpoint
  ParserVersion = "v1.0.0"
  Conditions = [ """Microsoft-Windows-Windows Defender/Operational""", """Windows Defender scan has finished"""]
  Fields = ${WindowsParsersTemplates.windows-defender-1.Fields}[
    """({event_name}Windows Defender scan has finished)"""
    ]

windows-defender-1 = {
  Vendor = "Microsoft"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"EventReceivedTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
    """Hostname":"({host}[^"]+?)""""
    """"+host"+:"+({host}[^"]+)"+"""
    """"+@version"+:"+({version}[^"]+)"+"""
# system_info is removed
    """Severity":"({severity}[^"]+?)""""
    """AccountType":"({user_type}[^"]+?)""""
    """Message":"({additional_info}[^"]+?)\s*""""
    """AccountName":"({user}[^"]+?)""""
    """EventID":({event_code}\d+)"""
    """EventType":"({operation_type}[^"]+?)""""
# src_name is removed
 
}
```