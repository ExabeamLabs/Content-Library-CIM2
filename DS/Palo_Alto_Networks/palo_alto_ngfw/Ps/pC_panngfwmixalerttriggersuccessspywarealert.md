#### Parser Content
```Java
{
Name = "pan-ngfw-mix-alert-trigger-success-spywarealert"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """,THREAT,spyware,"""
]
Fields = [
  """,THREAT,spyware,[^,]+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """,THREAT,spyware,([^,]+,){2}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,"""
  """\d\d:\d\d:\d\d\s+({host}[\w\-.]+)"""
  """THREAT,({alert_type}[^,]+),"""
  """({alert_name}spyware)"""
  """,THREAT,spyware,([^,]*,){25}({action}[^,]+),"""
  """,THREAT,spyware,([^,]*,){26}\\?"+([^\(]+\()?(|({malware_url}[^\s".,]+(?:\.[^"\/\s,]+)?\/[^"]*?)|({malware_file_name}[^",]+))[\\\/]*"+,"""
  """,THREAT,([^,]*,){28}\d*(|({alert_name}[^\(,:]+))(:[^\(]+)?\(({alert_id}\d+)?"""
  """,THREAT,[^"]+?,\\?"[^\s]*?"+,?\d*(|({alert_name}[^,\("]+?))\s*\(({alert_id}\d+)?"""
  """,THREAT,[^"]+?,\\?"[^\s]*",[^,]*,({category}[^,]+),"""
  """THREAT,spyware,([^,]*,){29}({alert_severity}[^,]+)"""
  """THREAT,spyware,[^"]+?,\\?"[^\s]*?",([^,]*,){2}({alert_severity}[^,]+)"""
  """THREAT,spyware,([^,]*,){7}(({email_address}[^@,]+@[^\.,]+\.[^,]+)|(({domain}[^\\\/,]+)[\\\/]+)?({user}[^\\\/,]+)),"""
  """THREAT,spyware,([^,]*,){19}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),([^,]*,){3}(?:|({protocol}[^,]+)),(?:|({action}[^,]+)),\\?"*"""
  """THREAT,spyware,([^,]*,){9}({app}[^,]+),"""
  """,THREAT,[^"]+?,\\?"[^\s]*?"+,?([^"]+)"+,({alert_id}\d+)?"""
  """,({alert_severity}(?i)(low|medium|high|critical|informational)),({direction}[^,]*),([^,]+,){3}({src_location}[^\d,]+)?"""
  """THREAT,spyware,(("[^\s]+"|[^,]*),){64}(|""|({threat_category}[^,]+)),"""
  """,THREAT,spyware([^,]*,){27}(|(\\?"+(({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?)|({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+)),(|(\d+|({alert_name}[^,"]+?))\(({alert_id}\d+)?\)),(|({category}[^,]*)),(|({alert_severity}[^,]+)),("[^"]*",|[^,]*,){34}(|({threat_category}[^,]+)),"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
    "src_ip->malwareVictimHost"
    "alert_type->description"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
      ]
    

}
```