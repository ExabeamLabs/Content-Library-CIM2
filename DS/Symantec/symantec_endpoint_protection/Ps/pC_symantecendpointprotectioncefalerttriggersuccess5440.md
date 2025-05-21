#### Parser Content
```Java
{
Name = "symantec-endpointprotection-cef-alert-trigger-success-5440"
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""|310-2771385440|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|({alert_type}[^|]+?)\|"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|"""
"""\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sexternalId=({alert_id}\d+)"""
"""\sshost=({src_host}.+?)\s+\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\snitroThreat_Name =({alert_name}.+?)\s+\w+="""
"""\snitroDestination_Filename=({malware_url}.+?)\s+\w+="""
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
"src_host->malwareVictimHost"
"alert_type->description"
"malware_url->malwareAttackerUrl"
  ]
  NameTemplate = "Symantec Alert ${alert_name} found"
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