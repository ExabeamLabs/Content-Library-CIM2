#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-scan"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,scan,"""
]
Fields = [
  """THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))""",
  """:\d\d:\d\d\s+({host}[\w.-]+)\s"""
  """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,THREAT,({alert_type}[^,]+),([^,]*,){2}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),"""
  """,THREAT,([^,]*,){9}(({domain}[^\\,]+)\\+)?(({email_address}[^@,]+?@[^\.]+\.[^\\,]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),""",
  """,THREAT,([^,]*,){8}(({domain}[^\\,]+)\\+)?(({email_address}[^@,]+?@[^\.]+\.[^\\,]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),""",
  """,THREAT,([^,]*,){27}"?({malware_url}[^,"]+)"""
  """,THREAT,([^,]*,){27}(("[^"]*")|[^,]*),({alert_name}[^,]+),"""
  """,THREAT,([^,]*,){27}(("[^"]*")|[^,]*),([^,]*,){2}({alert_severity}[^,]+),"""
  """,THREAT,([^,]*,){27}(("[^"]*")|[^,]*),([^,]*,){4}({alert_id}\d+)"""
  """,THREAT,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),(?:[^,]*,){3}(?:|({protocol}[^,]+)),(?:|({action}[^,]*)),""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
  """THREAT,([^,]*,){4}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?,""",
  """THREAT,([^,]*,){5}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_translated_port}\d+))?,""",
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
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
    "src_ip->malwareVictimHost"
    "alert_type->malwareCategory"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
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
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
      ]
    

}
```