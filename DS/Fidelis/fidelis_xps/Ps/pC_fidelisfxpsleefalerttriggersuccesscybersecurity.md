#### Parser Content
```Java
{
Name = "fidelis-fxps-leef-alert-trigger-success-cybersecurity"
Vendor = "Fidelis"
Product = "Fidelis XPS"
TimeFormat = "epoch"
Conditions = [
"""LEEF:1.0|Fidelis Cybersecurity|"""
]
Fields = [
"""devTime=({time}\d{13})"""
"""dvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""dvchost=({host}.+?)\s*(\w+=|$)"""
"""cs1=({alert_name}.+?)\s*(\w+=|$)"""
"""cs1=({alert_type}.+?)\s*(\w+=|$)"""
"""proto=(Unknown|({alert_type}.+?))\s*(\w+=|$)"""
"""sev=({alert_severity}\d)"""
"""src=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""(srcPort|spt)=({src_port}\d+)"""
"""dst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""(dstPort|dpt)=({dest_port}\d+)"""
"""msg=\s*({additional_info}.+?)\s*(\w+=|$)"""
"""target=(?:(<n\/a>)|({malware_url}.+?))\s*(\w+=|$)"""
"""fname=(?:(<n\/a>)|({malware_url}.+?))\s*(\w+=|$).+?proto=SMB"""
"""duser=(?:(<n\/a>)|({target}.+?))(\s+\w+=|\s*$)"""
"""usrName =(?:(<n\/a>)|({email_address}.+?))(\s+\w+=|\s*$)"""
"""fname=(?:|(<n\/a>)|({process_name}.+?))\s+(\w+=|\s*$)"""
]
DupFields = [
"host->dest_host"
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"""time->startedDate"""
"""vendor->source"""
"""rawLog->sourceInfo"""
"""alert_name->malwareName"""
"""alert_type->malwareCategory"""
"""alert_severity->sourceSeverity"""
"""src_ip->malwareVictimHost"""
"""malware_url->malwareAttackerFile"""
"""dest_ip->malwareAttackerIp"""
  ]
  NameTemplate = "Fidelis Alert ${alert_name} found"
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