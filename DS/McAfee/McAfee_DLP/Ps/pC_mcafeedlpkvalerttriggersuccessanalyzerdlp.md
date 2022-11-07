#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-analyzerdlp
	ParserVersion = v1.0.0
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """AnalyzerName ="Data Loss Prevention"""","""ThreatCategory=""" ]
    Fields = [
      """ReceivedUTC="?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """ServerID="({host}[^"]+?)"""",
      """SourceHostName ="({src_host}[^"]+?)"""",
      """TargetHostName ="({dest_host}[^"]+?)"""",
      """TargetProcessName ="({process_path}[^"]+?[\\\/]({process_name}[^"\\\/]*))"""",
      """SourceProcessName ="({process_path}[^"]+?[\\\/]({process_name}[^"\\\/]*))"""",
      """TargetUserName ="(({domain}[^"\\\/]+?)[\\\/]+)?({user}[^"]+)"""",
      """SourceUserName ="(({domain}[^"\\\/]+?)[\\\/]+)?({user}[^"]+)"""",
      """ThreatSeverity="({alert_severity}\d+)""",
      """ThreatName ="({alert_name}[^"]+?)"""",
      """ThreatType="({alert_type}[^"]+?)"""",
      """ThreatEventID="({alert_id}\d+)""",
      """SourceIPV4="({src_ip}[^"]+)""",
      """TargetIPV4="({dest_ip}[^"]+)"""
    ]
  

}
```