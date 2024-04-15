#### Parser Content
```Java
{
Name = "pan-ngfw-mix-alert-trigger-success-virus"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """,THREAT,virus,"""
]
Fields = [
  """"host":\{[^=]*?"name":"({host}[^"]+)"[^=]*?\}"""
  """({host}[\w\-\.]+)\s+\d+,[^,]*,[^,]*,THREAT,virus,"""
  """,THREAT,([^,]*.){55}({host}[^,]+),"""
  """,THREAT(,[^,]*){40},("[^"]*",)([^,]*,){3}("[^"]*",){5}([^,]*,){6}({host}[^,]+)."""
  """THREAT,({alert_type}virus),\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),([^,]*,){3}(({domain}[^\\,]+)\\)?(?:|({user}[^,]+)),(({dest_domain}[^\\,]+)\\)?(?:|({dest_user}[^,]+)),"""
  """,THREAT,([^,]*,){26}({action}[^,]+),"""
  """,THREAT,([^,]*,){27}\\?"(|({malware_url}[^\s]+?))\\?","""
  """,THREAT,.+?,\\?"(|({file_name}[^\s]+?))\\?","""
  """,THREAT,.+?,\\?"[^"]*",({alert_name}[^,]+),"""
  """,THREAT,.+?,\\?"[^"]*",[^,]*,"?(unknown|({category}[^,"]+))"?,"""
  """,THREAT,([^,]*,){29}({category}[^,]+),"""
  """THREAT,virus,.+?,\\?"[^"]*",([^,]*,){2}({alert_severity}[^,]+),"""
  """THREAT,virus,.+?,\\?"[^"]*",([^,]*,){4}({alert_id}[^,]+),"""
  """,({alert_severity}(?i)(low|medium|high|critical|informational)),({direction}[^,]*),([^,]+,){3}({src_location}[^\d,]+)?"""
  """THREAT,virus,(("[^"]+?"|[^,]*),){64}({threat_category}[^,]+),"""
  """,THREAT,([^,]*,){28}(\d+|({alert_name}[^\(,]+?))\(({alert_id}\d+)?"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "src_ip->malwareVictimHost"
    "alert_id->sourceId"
    "alert_type->malwareCategory"
    "malware_url->malwareAttackerUrl"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
      ]
    

}
```