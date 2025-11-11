#### Parser Content
```Java
{
Name = "f5-asm-cef-alert-trigger-success-http"
Vendor = "F5"
Product = "F5 Application Security Manager"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """CEF:"""
  """ ASM:"""
  """|F5|ASM|"""
  """HTTP"""
]
Fields = [
  """rt=({time}\w+\s+\d\d\s+\d\d\d\d\s+\d\d:\d\d:\d\d)"""
  """dvc=({host}[A-Fa-f:\d.]+)"""
  """dvchost=({host}[\w\-.]+)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """spt=({src_port}\d+)"""
  """dpt=({dest_port}\d+)"""
  """act=({result}[^\s]+)\s+(\w+=|$)"""
  """cs4=(N/A|({alert_name}[^=]+))\s+(\w+=|$)"""
  """app=({protocol}[^=]+)\s+(\w+=|$)"""
  """request=({malware_url}[^\s]+)\s+(\w+=|$)"""
  """externalId=({alert_id}[^=]+)\s+(\w+=|$)"""
  """User-Agent:\s+({user_agent}[^\"]+?)\\r\\n"""
  """CEF:([^\|]+\|){4}(\d+\|)?({alert_type}[^\|]+)"""
  """CEF:([^\|]+\|){6}({alert_severity}\d+)"""
  """"username":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """Host:\s*({web_domain}[\w\-\.]+?)((\\r\\n|\s+)[\w\-]+:|\")"""
  """Referer:\s*({referrer}[^"]+?)((\\r\\n|\s+)[\w\-]+:|\")"""
]
SOAR {
  IncidentType = "malware"
   DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_type->malwareCategory"
    "malware_url->malwareAttackerFile"
    "dest_ip->malwareAttackerIp"
    "alert_id->sourceId"
  ]
  NameTemplate = "F5 Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
      ]
    

}
```