#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-mailfilter
  Vendor = McAfee
  Product = McAfee DLP Endpoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """AnalyzerName: """, """ThreatCategory: ""mail.filter""" ]
  Fields = [
    """[=\s^]DetectedUTC:\s"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """[=\s^]ServerID:\s"*({host}[\w\-.]+)"""",
    """[=\s^]AnalyzerHostName:\s"*({dest_host}[\w\-.]+)"""",
    """[=\s^]TargetHostName:\s"*(null|({dest_host}[\w\-.]+))"""",
    """[=\s^]SourceHostName:\s"*(null|({src_host}[\w\-.]+))"""",
    """[=\s^]TargetIPV4:\s"*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """[=\s^]SourceIPV4:\s"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """[=\s^]SourceUserName:\s"*({additional_info}[^"]+)"""",
    """[=\s^]TargetUserName:\s"*({target}[^"]+)"""",
    """[=\s^]TargetUserName:\s"*({target_1}[^"\s;]+)""",
    """[=\s^]ThreatType:\s"*({alert_name}[^"]+)""",
    """[=\s^]ThreatCategory:\s"*({alert_type}[^"]+)"""",
    """[=\s^]TargetFileName:\s"*\S+\|(Unknown filename|({file_name}[^\.\\]+(\.({file_ext}[^\.\\]+))[\.\w\\]*))""",
    """[=\s^]ThreatEventID:\s"*({alert_id}\d+)""",
    """[=\s^]ThreatSeverity:\s"*({alert_severity}[^"]+)""",
    """[=\s^]ThreatActionTaken:\s"*({result}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```