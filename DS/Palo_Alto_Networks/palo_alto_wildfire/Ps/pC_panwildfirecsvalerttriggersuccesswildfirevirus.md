#### Parser Content
```Java
{
Name = "pan-wildfire-csv-alert-trigger-success-wildfirevirus"
Vendor = "Palo Alto Networks"
Product = "Palo Alto WildFire"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,wildfire-virus,"""
]
Fields = [
  """THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))""",
  """\d\d:\d\d:\d\d\s({host}[\w.-]+)\s"""
  """THREAT,({alert_type}[^,]+),[^,]+,({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,([^,]*?,)"""
  """THREAT,({alert_type}[^,]+),(|([^,]+)),(|({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """THREAT,([^,]+,){2}({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """,THREAT,([^,]*?,){9}(?:\w+\\+)?(({email_address}[^@,]+@[^\.,]+\.[^,]+)|(({domain}[^\\,]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
  """,THREAT,([^,]*,){8}(({email_address}[^@,]+@[^\.,]+\.[^,]+)|(({domain}[^\\,]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
  """(?i),THREAT,(("[^"]*?",)|([^,]*,)){30,31}({alert_severity}low|medium|high|critical|informational),"""
  """,THREAT,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),([^,]*,){3}(?:|({protocol}[^,]+)),(?:|({action}[^,]*)),"""
  """,THREAT,([^,]*,){27}"[^"]*?",({alert_name}[^,]+?)\s*(\(({alert_id}\d+)\))?,"""
  """(?i),THREAT,(("[^"]*?",)|([^,]*,)){30,31}(low|medium|high|critical|informational),({direction}[^,]*),([^,]+,){3}({src_location}[^\d,]+)""",i
  """THREAT,([^,]*,){10}({app}[^,]*),""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
  """THREAT,([^,]*,){4}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?,""",
  """THREAT,([^,]*,){5}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_translated_port}\d+))?,""",
  """THREAT,([^,]*,){10}({network_app}[^,]+),""",
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
    "src_ip->malwareVictimHost"
    "alert_type->description"
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