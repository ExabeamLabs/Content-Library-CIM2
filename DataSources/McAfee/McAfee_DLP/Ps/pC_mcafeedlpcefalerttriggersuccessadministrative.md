#### Parser Content
```Java
{
Name = mcafee-dlp-cef-alert-trigger-success-administrative
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "epoch"
  Conditions = [ """McAfee|Data Loss Prevention""", """|Administrative: """ ]
  Fields = [
    """(\s|\|)rt=({time}.+?)\s+([\w\.-]+=|$)""",
    """CEF:(.*?\|){4}({alert_type}.*?)\|"""
    """CEF:(.*?\|){5}({alert_name}.*?)\|"""
    """CEF:(.*?\|){6}({alert_severity}.*?)\|"""
    """(\s|\|)deviceSeverity=({alert_severity}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)shost=({src_host}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)src=({src_ip}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)ad.PrimaryUserAccountID=({user}[^\|\s@]+)""",
    """(\s|\|)suser=({user}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)sntdom=({domain}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)categoryOutcome=(\/)?({action}[^\|\s]+)"""
    """(\s|\|)eventId=({alert_id}\d+)\s"""
  ]


}
```