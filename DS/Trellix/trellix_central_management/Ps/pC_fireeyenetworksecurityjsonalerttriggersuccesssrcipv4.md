#### Parser Content
```Java
{
Name = "fireeye-networksecurity-json-alert-trigger-success-srcipv4"
Vendor = "Trellix"
Product = "Trellix Central Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""alertType":"""
"""_rule""""
""""severity":"""
""""srcipv4":"""
]
Fields = [
""""createDate.+?"id":\s*"({alert_id}[^"]+)""""
""""risk":\s*"({alert_severity}[^"]+)""""
""""updateDate":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""""
""""srcipv4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""srcipv6":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""srchost":\s*"({src_host}[^"]+)""""
""""message":\s*"({alert_name}[^"]+?)\s+\[({alert_type}[^"]+?)\]""""
""""virus":\s*"({alert_name}[^"]+)""""
""""devicename":\s*"({host}[^"]+)""""
""""srcport":\s*({src_port}\d+)"""
""""action":\s*"({result}[^"]+)""""
""""dstipv4":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""dstport":\s*({dest_port}\d+)"""
""""detail":.+?"uri":\s*"({malware_url}[^"]+)""""
""""description":\s*"({additional_info}[^"]+)""""
""""username":\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_name->malwareName"
"alert_id->sourceId"
"alert_type->malwareCategory"
"alert_severity->sourceSeverity"
"src_host->malwareVictimHost"
"dest_ip->malwareAttackerIp"
"malware_url->malwareAttackerUrl"
  ]
  NameTemplate = "FireEye Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
"""dest_ip->ip_address"""
      ]
    

}
```