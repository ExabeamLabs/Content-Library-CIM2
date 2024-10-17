#### Parser Content
```Java
{
Name = "vmware-carbonblack-cef-alert-trigger-success-activethreat"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|CarbonBlack|CbDefense_Syslog_Connector|"""
"""|Active_Threat|"""
]
Fields = [
"""(\s|\|)rt="({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""(\s|\|)dvc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\s|\|)dvchost=({host}[\w\-.]+)"""
"""(\s|\|)duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""([^\|]*\|){5}({alert_type}[^\|]+)"""
"""([^\|]*\|){6}({alert_name}[^\|]+)"""
"""([^\|]*\|){7}({alert_severity}\d+)"""
"""(\s|\|)cs4="({alert_id}[^"]+)"""
]
DupFields = [
"host->dest_host"
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->description"
"alert_severity->sourceSeverity"
"alert_id->sourceId"
"src_ip->malwareVictimHost"
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
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