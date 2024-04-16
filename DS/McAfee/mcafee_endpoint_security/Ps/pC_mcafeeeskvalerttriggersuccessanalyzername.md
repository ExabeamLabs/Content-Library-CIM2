#### Parser Content
```Java
{
Name = "mcafee-es-kv-alert-trigger-success-analyzername"
Vendor = "McAfee"
Product = "McAfee Endpoint Security"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "dd/MM/yyyy HH:mm:ss a"]
Conditions = [
  """AnalyzerName ="""
  """ThreatCategory="""
]
Fields = [
  """UTC=({time}\d+\/\d+\/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
  """ReceivedUTC="?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """ServerID="?({host}[^"\|]+?)("|\||\s\w+=)""",
  """TargetHostName ="?(?:|None|({src_host}[^"\|]+?)|)("|\||\s\w+=)""",
  """TargetIPV4="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """TargetUserName ="?(?:|None|(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))("|\||\s\w+=)""",
  """ThreatCategory="?({threat_category}[^"\|]+?)("|\||\s\w+=)""",
  """AutoGUID="?({alert_id}[^"]+?)("|\s+\w+=|\s*$)""",
  """ThreatSeverity="?({alert_severity}[^"\|]+?)("|\||\s\w+=)""",
  """ThreatName ="?(?:|none|({alert_name}[^"\|]+?))("|\||\s\w+=)""",
  """ThreatType="?(?:|none|({alert_type}[^"\|]+?))("|\||\s\w+=)""",
  """TargetFileName ="?(?:|None|({malware_url}.+?\\({malware_file_name}[^\\]+?)))("|\||\s\w+=)""",
  """OSType="({os}[^"]+)"""",
  """TargetProcessName ="?(?:|none|({process_name}[^"\|]+?))("|\||\s\w+=)""",
]
SOAR {
   IncidentType = "malware"
   DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_id->sourceId", "alert_name->malwareName", "src_host->malwareVictimHost", "malware_url->malwareAttackerUrl", "alert_type->malwareCategory", "threat_category->malwareCategory", "alert_severity->sourceSeverity", "malware_file_name->malwareAttackerFile"]
   NameTemplate = """McAfee EPO Alert ${alert_name} found"""
   ProjectName = "SOC"
   EntityFields = [
     {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```