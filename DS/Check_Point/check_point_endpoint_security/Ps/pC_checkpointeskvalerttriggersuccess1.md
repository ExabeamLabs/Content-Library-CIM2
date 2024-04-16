#### Parser Content
```Java
{
Name = "checkpoint-es-kv-alert-trigger-success-1"
Vendor = "Check Point"
Product = "Check Point Endpoint Security"
ParserVersion = "v1.0.0"
TimeFormat = "epoch_sec"
Conditions = [
"""product=VPN-1 & FireWall-1"""
"""|malware_action="""
]
Fields = [
"""date=({time}\d{10})"""
"""\|orig=({host}[^\|]+)\|"""
"""\|Protection name=({alert_name}[^\|]+)\|"""
"""\|malware_action=({alert_type}[^\|]+)\|"""
"""\|severity=({alert_severity}[^\|]+)\|"""
"""\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\|s_port=({src_port}\d+)"""
"""\|dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|service=({dest_port}\d+)"""
"""\|action=({action}[^\|]+)"""
"""\|proto=({protocol}[^\|]+)"""
"""\|src_machine_name=({src_host}[^\|]+)"""
"""\|description=({additional_info}[^\|]+)"""
"""\|src_user_name=[^(]+\(({user}[\w\.\-]{1,40}\$?)"""
"""\|user=[^(]+\(({user}[\w\.\-]{1,40}\$?)"""
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