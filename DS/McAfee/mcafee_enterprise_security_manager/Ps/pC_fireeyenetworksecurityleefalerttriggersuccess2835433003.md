#### Parser Content
```Java
{
Name = "fireeye-networksecurity-leef-alert-trigger-success-2835433003"
Vendor = "McAfee"
Product = "McAfee Enterprise Security Manager"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""|444-2835433003|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|"""
"""\|McAfee\|ESM\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|"""
"""\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sexternalId=({alert_id}\d+)"""
"""\sshost=({src_host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\snitroObjectID=({alert_type}.+?)\s+nitroAttacker_IP"""
"""\snitroURL=({additional_info}[^\r\n]+)\s+"""
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