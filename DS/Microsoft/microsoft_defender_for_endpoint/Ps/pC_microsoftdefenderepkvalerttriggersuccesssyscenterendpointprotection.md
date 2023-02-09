#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-alert-trigger-success-syscenterendpointprotection
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """vendor=Microsoft product="""
  """System Center Endpoint Protection"""
]
Fields = [
  """dest_name=({dest_host}[^\s]+)\s"""
  """action_time="({time}[^"]+)""""
  """alert_time="({time}[^"]+)""""
  """user_id=({user}[\w\d]+)\s+dest_ip=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+"""
  """severity=({alert_severity}[\w]+)\s+category=({alert_type}[^\s]+)\s+action"""
  """detection_id=({alert_id}[^\s]+)\s+"""
  """signature=({alert_name}[^\s]+)\s+"""
  """process="({process_path}[^"]+\\({process_name}[^"]+))""""
]
DupFields = [
  "dest_ip->src_ip"
  "dest_host->src_host"
  "process_name->file_name"
]
ParserVersion = "v1.0.0"


}
```