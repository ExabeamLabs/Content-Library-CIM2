#### Parser Content
```Java
{
Name = "morphisec-eptp-json-alert-trigger-success-attacktimedt"
Vendor = "Morphisec"
Product = "Morphisec"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""attack_module_s""""
""""attack_time_dt""""
]
Fields = [
"""({host}[\w\.-]+)\s+Morphisec-Server"""
""""attack_time_dt\"\s*:\s*\[\s*\"({time}[^\"]+)\""""
"""({alert_name}attack)"""
""""machine_s\"\s*:\s*\[\s*\"({src_host}[^\"]+)\""""
""""ip_addr_s\"\s*:\s*\[\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
""""application_s\"\s*:\s*\[\s*\"({malware_url}[^\"]+)\""""
""""user_s\"\s*:\s*\[\s*\"(({domain}[^\"]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
""""attack_module_s\"\s*:\s*\[\s*\"({attack_info}[^\"]+)\""""
""""suspicious_files_ss\"\s*:\s*\[\s*\[\s*(\"\"|({malware_file_name}.+?))\s*\]\s*\]\s*[,\]\}]"""
""""suspicious_urls_ss\"\s*:\s*\[\s*\[\s*(\"\"|({malware_url}.+?))\s*\]\s*\]\s*[,\]\}]"""
]
DupFields = [
"alert_name->alert_type"
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
"""suspicious_files->malwareAttackerFile"""
  ]
  NameTemplate = "Morphisec Alert ${alert_name} found"
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