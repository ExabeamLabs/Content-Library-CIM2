#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-flood"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,flood,"""
]
Fields = [
  """THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))""",
  """\s+({host}[\w\-\.]+)(\/[A-F:\da-f\.]+)?\s+\d+,[^"]+?,THREAT,flood,""",
  """THREAT,[^,]+,\d+,({time}\d+/\d+/\d+\s+\d\d:\d\d:\d\d),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,([^,]*?,){21}({alert_type}[^,]*),"*({malware_url}[^",]+)?"*,([^,]+?),[^,]+?,({alert_severity}[^,]+?),({additional_info}[^,]+),({alert_id}\d+)"""
  """,THREAT,([^,]*,){28}({alert_name}[^,]+),""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  """THREAT,([^,]*,){4}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?,""",
  """THREAT,([^,]*,){5}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_translated_port}\d+))?,""",
  """THREAT,([^,]*,){10}(not-applicable|({network_app}[^,]+)),""",
  """THREAT,([^,]*,){12}({src_network_zone}[^,]+),""",
  """THREAT,([^,]*,){13}({dest_network_zone}[^,]+),""",
  """THREAT,([^,]*,){14}({src_interface}[^,]+),""",
  """THREAT,([^,]*,){15}({dest_interface}[^,]+),""",
  """({serial_num}[^,]+),THREAT,"""
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