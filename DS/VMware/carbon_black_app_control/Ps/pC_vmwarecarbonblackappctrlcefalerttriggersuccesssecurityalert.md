#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-cef-alert-trigger-success-securityalert"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Bit9|"""
"""|Security alert|"""
]
Fields = [
"""\|Bit9(\|[^\|]+){3}\|({alert_name}[^\|]+)\|"""
"""cat=({alert_type}.+?)\s+\w+="""
"""\|({alert_severity}[^\|]+)\|\w+="""
"""externalId=({alert_id}\d+)"""
"""dst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dhost=([^\\]+\\+)?({src_host}[\w\-.]+)\s*(\w+=|$)"""
"""dvchost=([^\\]+\\+)?({host}[^\s]+)\s+\w+="""
"""filePath=({malware_url}.+?)\s+\w+="""
"""filePath=({malware_url_path}\w+:\/\/.+?)\s+\w+="""
"""filePath=(?!\w+:\/\/)({process_path}.+?)\s+\w+="""
"""msg=({additional_info}.+?)\s+\w+="""
"""fname=({process_name}.*?)\s\w+="""
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
"malware_url_path->malwareAttackerUrl"
"file_path->malwareAttackerFile"
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
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