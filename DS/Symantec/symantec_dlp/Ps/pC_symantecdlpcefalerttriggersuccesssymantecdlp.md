#### Parser Content
```Java
{
Name = symantec-dlp-cef-alert-trigger-success-symantecdlp
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "epoch"
Conditions = [
"""CEF"""
"""|Symantec|DLP|"""
]
Fields = [
"""({host}[\w\-.]+)\s+CEF:"""
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[\w.\-]+)"""
"""\ssuser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\shost=({src_host}.+?)\s\w+="""
"""\W(externalId|INCIDENT_ID)=({alert_id}\d+)"""
"""\|Symantec\|DLP\|([^|]*\|){3}({alert_severity}[^|]+)\|"""
"""\|Symantec\|DLP\|([^|]*\|){2}({alert_name}[^|]+)\|"""
"""\|Symantec\|DLP\|([^|]*\|){2}({alert_type}[^|]+)\|"""
"""\|Symantec\|DLP\|([^|]*\|){2}.*?({protocol}[^\s|]+)\|"""
"""\sdeviceSeverity=\d:({alert_severity}.+?)\s\w+="""
"""SEVERITY=\d:({alert_severity}[^\s]+)"""
"""\scat=({alert_type}.+?)\s\w+="""
"""\sapp=({alert_type}.+?)\s\w+="""
"""\sfname=(?:N\/A|({file_name}.+?))\s\w+="""
"""\sfilePath=(?:N\/A|({process_dir}.+?))\s\w+="""
"""\smsg=(?:N\/A|({additional_info}.+?))\s\w+="""
"""\W(act|BLOCKED)=(?:None|({action}.+?))\s\w+="""
"""\WSENDER=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
"""\WSENDER=(N\/A|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\s@]*?(({domain}[^\\\/\s@]+)[\\\/]+)?({user}[^\\\/\s@]+))\s+(\w+=|$)"""
"""\WENDPOINT_MACHINE=({src_host}[\w\-.]+)\s+(\w+=|$)"""
"""\WPROTOCOL=(N\/A|({protocol}.+?))\s+(\w+=|$)"""
]
DupFields = [
"email_address->src_email_address"
]
SOAR {
  IncidentType = "dlp"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"user->dlpUser"
"alert_name->dlpPolicy"
"alert_severity->sourceSeverity"
"protocol->dlpProtocol"
"src_host->dlpDeviceName"
"file_name->dlpFileName"
"action->dlpActionTaken"
  ]
  NameTemplate = "Symantec DLP Alert ${alert_name} found"
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