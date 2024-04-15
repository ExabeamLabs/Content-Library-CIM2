#### Parser Content
```Java
{
Name = "fidelis-fnetwork-cef-alert-trigger-success-alertid"
Vendor = "Fidelis"
Product = "Fidelis Network"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Product="Fidelis network""""
"""AlertId="""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[^\s]+)\s+Product="""
"""\sPolicy=\"({alert_name}[^\"]+)\""""
"""\sProtocol=\"({alert_type}[^\"]+)\""""
"""\sSeverity=\"({alert_severity}[^\"]+)\""""
"""\sSrcIP=\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""\sSrcPort=\"({src_port}\d+)\""""
"""\sDestIP=\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\sDestPort=\"({dest_port}\d+)\""""
"""\sMessage=\"({additional_info}.+?)\"\s+MD5=\""""
"""\sTarget=\"(?:(<n\/a>)|({malware_url}[^\"]+))\""""
"""\sMalware=\"(?:(<n\/a> <n\/a>)|({malware_url}[^\"]+))\""""
"""\sSubject=\"(?:(<n\/a>)|({malware_url}[^\"]+))\""""
"""\sFilename=\"(?:(<n\/a>)|({malware_url}[^\"]+))\""""
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