#### Parser Content
```Java
{
Name = "microsoft-defenderep-str-app-notification-versionupdated"
  Product = Microsoft Defender for Endpoint
  Conditions = [ 
    """Microsoft-Windows-Windows Defender/Operational"""
    """Defender Antivirus Security intelligence version has been updated"""
  ]
  Fields = ${WindowsParsersTemplates.windows-defender-1.Fields}[
    """({event_name}Defender Antivirus Security intelligence version has been updated)"""
  ]
  ParserVersion = "v1.0.0"

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