#### Parser Content
```Java
{
Name = "checkpoint-es-kv-alert-trigger-success-threatemulation"
Vendor = "Check Point"
Product = "Check Point Endpoint Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""product=Threat Emulation"""
"""|malware_action="""
]
Fields = [
"""time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\|orig=({host}[^\|]+)\|"""
"""\|Protection Name =({alert_name}[^\|]+)\|"""
"""Malware signature matched \(\s*({alert_name}.+?)\s*\)"""
"""\|Protection Type=({alert_type}[^\|]+)\|"""
"""\|severity=({alert_severity}[^\|]+)\|"""
"""\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\|s_port=({src_port}\d+)"""
"""\|dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|service=({dest_port}\d+)"""
"""\|action=({action}[^\|]+)"""
"""\|proto=({protocol}[^\|]+)"""
"""\|file_md5=({hash_md5}[^\|]+)"""
"""\|malware_action=({additional_info}[^\|]+)"""
"""\|action=({action}[^\|]+)"""
"""\|file_name=({file_name}[^\|]+)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_type->malwareCategory"
"alert_severity->sourceSeverity"
"src_ip->malwareVictimHost"
"dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Check Point Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
"""src_ip->ip_address"""
      ]
    

}
```