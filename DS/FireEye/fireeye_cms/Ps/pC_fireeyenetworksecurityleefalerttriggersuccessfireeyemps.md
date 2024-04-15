#### Parser Content
```Java
{
Name = "fireeye-networksecurity-leef-alert-trigger-success-fireeyemps"
Vendor = "FireEye"
Product = "FireEye CMS"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""LEEF:"""
"""FireEye|MPS"""
]
Fields = [
"""devTime=({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\^"""
"""dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\^"""
"""dvchost=({host}[^\^]+)\^"""
"""shost=({src_host}[^\^]+)\^"""
"""sname=({alert_name}[^\^]+)\^"""
"""FireEye\|MPS\|[^\|]+\|({alert_type}[^\|]+)\|sev=({alert_severity}[^\^]+)\^"""
"""externalId=({alert_id}[^\^]+)\^"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_id->sourceId"
"alert_type->malwareCategory"
"alert_severity->sourceSeverity"
"src_host->malwareVictimHost"
"dest_ip->malwareAttackerIp"
  ]
    NameTemplate = "FireEye Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
"""src_ip->ip_address"""
"""src_host->host_name"""
      ]
    

}
```