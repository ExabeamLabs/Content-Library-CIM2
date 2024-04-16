#### Parser Content
```Java
{
Name = "blackberry-protect-json-alert-trigger-success-cylancescore"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
ExtractionType = json
TimeFormat = "M/d/yyyy H:mm:ss a"
Conditions = [
""""Cylance Score""""
""""Malware - """
""""Tenant""""
]
Fields = [
"""exa_json_path=$.['Access Time'],exa_field_name=time"""
"""exa_json_path=$.['Device Name'],exa_field_name=host"""
"""exa_json_path=$.DeviceName,exa_field_name=host"""
"""exa_json_path=$.Classification,exa_field_name=alert_name"""
"""exa_json_path=$.['File Owner'],exa_regex=((N/A)|(({domain}[^\\]+)\\+({user}[\w\.\-]{1,40}\$?)))""",
"""exa_json_path=$.['File Status'],exa_field_name=additional_info"""
"""exa_json_path=$.['Cylance Score'],exa_field_name=alert_severity"""
"""exa_json_path=$.['File Path'],exa_field_name=malware_url"""
"""exa_json_path=$.['File Name'],exa_field_name=file_name"""
]
DupFields = [
"alert_name->alert_type"
"host->src_host"
"file_name->process_name"
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_type->malwareCategory"
"src_host->malwareVictimHost"
"alert_severity->sourceSeverity"
"malware_url->malwareAttackerFile"
  ]
  NameTemplate = "Cylance Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
"""src_host->host_name"""
      ]
    

}
```