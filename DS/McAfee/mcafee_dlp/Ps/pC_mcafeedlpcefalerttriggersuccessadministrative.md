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
    """(\s|\|)rt=({time}\d{13})\s+([\w\.-]+=|$)""",
    """CEF:(.*?\|){4}({alert_type}.*?)\|"""
    """CEF:(.*?\|){5}({alert_name}.*?)\|"""
    """CEF:(.*?\|){6}({alert_severity}.*?)\|"""
    """(\s|\|)deviceSeverity=({alert_severity}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)shost=({src_host}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+([\w\.-]+=|$)""",
    """(\s|\|)ad.PrimaryUserAccountID=({user}[^\|\s@]+)""",
    """(\s|\|)suser=({user}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)sntdom=({domain}.+?)\s+([\w\.-]+=|$)""",
    """(\s|\|)categoryOutcome=(\/)?({action}[^\|\s]+)"""
    """(\s|\|)eventId=({alert_id}\d+)\s"""
  ]


}
```