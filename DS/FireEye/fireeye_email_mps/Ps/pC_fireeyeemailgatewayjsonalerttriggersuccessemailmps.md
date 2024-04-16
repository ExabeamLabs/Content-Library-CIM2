#### Parser Content
```Java
{
Name = "fireeye-emailgateway-json-alert-trigger-success-emailmps"
Vendor = "FireEye"
Product = "FireEye Email MPS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
ExtractionType = json
Conditions = [
""""msg": """"
""""product": "Email MPS""""
""""alert": {"""
"""malware-detected"""
]
Fields = [
"""exa_json_path=$.appliance,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$.alert.dst.smtp-to,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
"""exa_json_path=$.alert.src.smtp-mail-from,exa_regex=^({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
"""exa_json_path=$.alert.explanation.malware-detected.malware.name,exa_field_name=alert_name""",
"""exa_regex=({alert_type}malware-detected)""",
"""exa_json_path=$.alert.severity,exa_field_name=alert_severity""",
"""exa_json_path=$.alert.occurred,exa_field_name=time""",
"""exa_json_path=$.alert.id,exa_field_name=alert_id""",
"""exa_json_path=$.alert.alert-url,exa_field_name=additional_info""",
"""exa_json_path=$.alert.action,exa_field_name=result""",
"""exa_json_path=$.alert.explanation.malware-detected.malware.md5sum,exa_field_name=hash_md5""",
"""exa_regex=({category}Email)"""
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