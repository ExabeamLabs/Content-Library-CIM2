#### Parser Content
```Java
{
Name = "pan-wildfire-csv-alert-trigger-success-correlationalert"
Vendor = "Palo Alto Networks"
Product = "Palo Alto WildFire"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,CORRELATION,"""
]
Fields = [
  """\d\d:\d\d:\d\d(\.\d+Z)? ({host}[\w\-.]+)"""
  """\s*({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d+Z)"""
  """,CORRELATION,([^,]*,){2}({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """,CORRELATION,([^,]*,){4}(|(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
  """,CORRELATION,([^,]*,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """,CORRELATION,([^,]*,){15}({alert_name}[^,]+)"""
  """,CORRELATION,([^,]*,){6}({alert_type}[^,]+)"""
  """,CORRELATION,([^,]*,){7}({alert_severity}[^,]+)"""
  """,CORRELATION,([^,]*,){17}\\?"*\s*({additional_info}({alert_name}[^\.,]+)[^\.]*)\."""
  """\d\d:\d\d:\d\d,({alert_id}[^,]+),"""
  """Process Name: ({malware_url}[^,]+),""",
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
    "alert_id->sourceId"
    "src_ip->malwareVictimHost"
    "alert_type->description"
    "malware_url->malwareAttackerUrl"
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