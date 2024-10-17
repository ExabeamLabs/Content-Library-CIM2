#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-leef-alert-trigger-success-securityplatform"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Conditions = [
"""|Bit9|Security_Platform|"""
"""|cat="""
]
Fields = [
"""\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
"""LEEF:([^\|]*\|){4}({alert_name}[^\|]+)"""
"""({host}[\w\-.]+)\s*LEEF:"""
"""\Wsev=({alert_severity}\d+)"""
"""\WusrName =(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WsrcHostName =(({domain}[^\\]+)\\+)?({src_host}[\w\-.]+)"""
"""\WdstHostName =({dest_host}[\w\-.]+)"""
"""\WsrcProcess=({process_path}({process_dir}([^=]+)?[\\\/])?({process_name}[^\\\/=]+?))\s*(\w+=|$)"""
"""\WfilePath=({file_path}.+?)\s*(\w+=|$)"""
"""\WfileName =({file_name}.+?)\s*(\w+=|$)"""
"""\WinstallerFileName =({additional_info}.+?)\s*(\w+=|$)"""
]
DupFields = [
"alert_name->alert_type"
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_severity->sourceSeverity"
"src_host->malwareVictimHost"
"alert_type->description"
"file_path->malwareAttackerFile"
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
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