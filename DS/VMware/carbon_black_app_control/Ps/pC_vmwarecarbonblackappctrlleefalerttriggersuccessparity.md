#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-leef-alert-trigger-success-parity"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """LEEF:"""
  """Bit9|Parity"""
]
Fields = [
  """\|cat=(?!General Management).+?devTime=({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)"""
  """Bit9\|Parity\|[^\|]+\|({alert_name}[^\|]+)\|cat=({alert_type}.+?)\s+sev"""
  """sev=({alert_severity}[\d]+)"""
  """externalId=({alert_id}[\d]+)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """srcHostName =({domain}[^\\]+)\\?({src_host}[^\s]+)"""
  """usrName =({user}[\w\.\-]{1,40}\$?)"""
  """filePath=({malware_url}.+?)\s+fileName"""
  """filePath=({malware_url_path}\w+:\/\/.+?)\s+fileName"""
  """filePath=({file_path}(?!\w+:\/\/).+?)\s+fileName"""
  """dstHostName =({dest_host}[^\s]+)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
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
        "src_ip->ip_address"
        "src_host->host_name"
      ]
    

}
```