#### Parser Content
```Java
{
Name = "fireeye-emailgateway-json-alert-trigger-success-emailmps"
Vendor = "FireEye"
Product = "FireEye Email MPS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""msg": """"
""""product": "Email MPS""""
""""alert": {"""
"""malware-detected"""
]
Fields = [
""""appliance": "({host}[^"]+)""""
""""smtp-to": "({email_address}[^"@]+?@({domain}[^"]+))""""
""""smtp-mail-from": "({src_email_address}[^"@]+?@[^"]+)""""
""""malware": \{.*?"name": "({alert_name}[^"]+)""""
"""({alert_type}malware-detected)"""
""""severity": "({alert_severity}[^"]+)""""
""""occurred": "({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""""
""""id": "({alert_id}[^"]+)","""
""""alert-url": "({additional_info}[^"]+)""""
""""action": "({result}[^"]+)""""
""""md5sum": "({hash_md5}[^"]+)""""
"""({category}Email)"""
]
DupFields = [
"alert_name->malware_file_name"
"email_address->dest_email_address"
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
"additional_info->sourceUrl"
  ]
  NameTemplate = "FireEye Email MPS Alert ${alert_name} found"
  ProjectName = "SOC"


}
```