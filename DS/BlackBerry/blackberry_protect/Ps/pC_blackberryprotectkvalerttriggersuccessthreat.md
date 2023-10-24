#### Parser Content
```Java
{
Name = "blackberry-protect-kv-alert-trigger-success-threat"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
Conditions = [
"""Event Type: Threat"""
"""Is Running: """
"""Cylance Score: """
]
Fields = [
"""\[({host}[\w\-.]+)\]\s*Event Type:"""
"""Date: ({time}\d+\/\d+\/\d+ \d+:\d+:\d+ \w+)"""
"""File Name: ({malware_url}[^,]+)"""
"""Event Type:\s*({alert_type}[^,]+)"""
"""Event Name: ({alert_name}[^,]+)"""
"""Cylance Score: ({alert_severity}\d+)"""
"""Device Name: ({src_host}[^,]+)"""
"""IP Address: \(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Path: ({process_dir}[^,]+)\\({process_name}[^,]+)?"""
"""Threat Classification:\s*({alert_name}[^,]+),"""
"""Status:\s*({result}[^,]+),"""
"""MD5:\s*({hash_md5}[^,]+),"""
"""File Owner:\s*(({domain}[^\\,]+)\\)?({user}[\w\.\-]{1,40}\$?),"""
"""SHA256:\s*({hash_sha256}[^,]+),"""
"""Detected By:\s*({additional_info}[^,]+?)\s*(\w+=|,|"\s*$)"""
]
DupFields = [
"malware_url->process_name"
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"""time->startedDate"""
"""vendor->source"""
"""rawLog->sourceInfo"""
"""alert_name->malwareName"""
"""alert_type->malwareCategory"""
"""src_host->malwareVictimHost"""
"""alert_severity->sourceSeverity"""
"""malware_url->malwareAttackerFile"""
  ]
  NameTemplate = "Cylance Alert ${alert_name} found"
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