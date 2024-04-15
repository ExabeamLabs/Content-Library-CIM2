#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-flood"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """,THREAT,flood,"""
]
Fields = [
  """\s+({host}[\w\-\.]+)(\/[A-F:\da-f\.]+)?\s+\d+,[^"]+?,THREAT,flood,"""
  """THREAT,[^,]+,\d+,({time}\d+/\d+/\d+\s+\d\d:\d\d:\d\d),({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,([^,]*?,){21}({alert_type}[^,]*),"*({malware_url}[^",]+)?"*,([^,]+?),[^,]+?,({alert_severity}[^,]+?),({additional_info}[^,]+),({alert_id}\d+)"""
  """,THREAT,([^,]*,){28}({alert_name}[^,]+),"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_id->sourceId"
    "alert_severity->sourceSeverity"
    "src_ip->malwareVictimHost"
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