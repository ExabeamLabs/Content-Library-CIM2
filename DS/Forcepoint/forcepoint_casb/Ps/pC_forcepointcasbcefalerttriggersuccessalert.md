#### Parser Content
```Java
{
Name = "forcepoint-casb-cef-alert-trigger-success-alert"
Vendor = "Forcepoint"
Product = "Forcepoint CASB"
TimeFormat = "epoch"
Conditions = [
"""CEF"""
"""Skyfence"""
"""|Alert|"""
]
Fields = [
"""\sdvc="+({host}[^"]+)"""
"""\sdvchost="+({host}[^"]+)"""
"""\srt="+({time}\d{13})"""
"""\sduser="+({user}[^"@]+)"""
"""\sduser="+[^@"]+@({domain}[^".]+)"""
"""\scat="+({alert_name}[^"/]+)"""
"""\sapp="+({alert_type}[^"]+)"""
"""0\|[^|]+?\|Alert\|({alert_severity}\d+)"""
"""\sdst="+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\ssrc="+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\srequest="+({additional_info}[^"]+)"""
]
SOAR {
  IncidentType = "generic"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->description"
"alert_severity->sourceSeverity"
  ]
  NameTemplate = "Skyfence Alert ${alert_name} found"
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