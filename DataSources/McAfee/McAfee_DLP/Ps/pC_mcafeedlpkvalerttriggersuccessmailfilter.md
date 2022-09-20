#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-mailfilter
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """AnalyzerName: """, """ThreatCategory: ""mail.filter""" ]
  Fields = [
    """[=\s^]DetectedUTC:\s"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """[=\s^]ServerID:\s"*({host}[\w\-.]+)"""",
    """[=\s^]AnalyzerHostName:\s"*({dest_host}[\w\-.]+)"""",
    """[=\s^]TargetHostName:\s"*(null|({dest_host}[\w\-.]+))"""",
    """[=\s^]SourceHostName:\s"*(null|({src_host}[\w\-.]+))"""",
    """[=\s^]TargetIPV4:\s"*({dest_ip}[A-Fa-f:\d.]+)""",
    """[=\s^]SourceIPV4:\s"*({src_ip}[A-Fa-f:\d.]+)""",
    """[=\s^]SourceUserName:\s"*({additional_info}[^"]+)"""",
    """[=\s^]TargetUserName:\s"*({target}[^"]+)"""",
    """[=\s^]TargetUserName:\s"*({target_1}[^"\s;]+)""",
    """[=\s^]ThreatType:\s"*({alert_name}[^"]+)""",
    """[=\s^]ThreatCategory:\s"*({alert_type}[^"]+)"""",
    """[=\s^]TargetFileName:\s"*\S+\|(Unknown filename|({file_name}[^"]+))""",
    """[=\s^]ThreatEventID:\s"*({alert_id}\d+)""",
    """[=\s^]ThreatSeverity:\s"*({alert_severity}[^"]+)""",
    """[=\s^]ThreatActionTaken:\s"*({action}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```