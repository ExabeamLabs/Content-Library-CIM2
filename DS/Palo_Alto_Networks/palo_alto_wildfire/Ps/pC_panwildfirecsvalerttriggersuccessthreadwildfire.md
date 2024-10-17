#### Parser Content
```Java
{
Name = "pan-wildfire-csv-alert-trigger-success-threadwildfire"
Vendor = "Palo Alto Networks"
Product = "Palo Alto WildFire"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,wildfire"""
]
Fields = [
  """\d\d:\d\d:\d\d\s({host}[\w.-]+)\s"""
  """THREAT,({alert_type}[^,]+),[^,]+,({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,([^,]*?,)"""
  """THREAT,({alert_type}[^,]+),[^,]+,({time}\d+\/\d+\/\d+ \d+:\d+:\d+),({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
  """THREAT,([^,]+,){2}({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """,THREAT,([^,]*?,){9}(?:\w+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?),"""
  """,THREAT,([^,]*,){8}(({email_address}[^@,]+@[^\.,]+\.[^,]+)|(({domain}[^\\,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
  """,({alert_severity}(?i)(low|medium|high|critical|informational)),"""
  """,THREAT,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),([^,]*,){3}(?:|({protocol}[^,]+)),(?:|({action}[^,]*)),"""
  """(?i),THREAT,(("[^"]*?",)|([^,]*,)){30,31}(?i)(low|medium|high|critical|informational),({direction}[^,]*),([^,]+,){3}({src_location}[^\d,]+)"""
  """,THREAT,(([^"]+?"[^"]+",)|([^,]*,){28})(({alert_name}[^,]+?)\()?({alert_id}\d+)?\)?,"""
  """,THREAT,(?:[^,]*,){46}({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)),(([\/\\"]*({alert_subject}[^"]+?)[\/\\"]+)|(|({=alert_subject}[^,]+?))),({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)),""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
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