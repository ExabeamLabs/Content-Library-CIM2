#### Parser Content
```Java
{
Name = "fireeye-networksecurity-cef-alert-trigger-success-trellix-1"
Vendor = "Trellix"
Product = "Trellix Central Management"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """CEF:"""
  """|Trellix|"""
]
Fields = [
  """rt=({time}[a-zA-Z]{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
  """externalId=({alert_id}\d+)""",
  """\|Trellix\|([^\|]+\|){3}({alert_type}[^\|]+)\|({alert_severity}[^\|]+)\|""",
  """\|Trellix\|([^\|]+\|){3}({alert_name}[^\|]+)\|""",
  """\ssrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """\sshost=({dest_host}[\w\-\.]+)""",
  """\sfilePath=(?:({malware_url}[^\s.]+\.[^\/\s]+\/[^=]+?)|({malware_file_name}[^=]+?))\s\w+=""",
  """\scs1Label=sname cs1=({alert_name}[^=]+?)\s\w+=""",  
  """\scs5Label=cncHost cs5=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+))""",
  """\srequest=({malware_url}[^\s]+)""",
  """\sdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """\sdhost=({src_host}[\w\-\.]+)""",
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^\s]+)?\s+cn1Label""",
  """\Wdvc=(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))"""
  """\sdvchost=({host}[\w\-\.]+)""",
  """\sact=({action}[^=]+?)\s+\w+=""",
  """categoryOutcome=(\/)?({result}[^\s]+)"""
  """CEF:([^\|]*\|){4}({event_name}({operation}[^\|]+))""",
  """request=({object}({resource}[^\s=]+))\s*(\w+=|$)"""
  """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """act=({category}[^=]+)\s+\w+="""
  """msg=({additional_info}[^=]+)\s+\w+=""",
  """Trellix\|({app}[^\|]+)\|"""
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
    "src_host->malwareVictimHost"
    "malware_file_name->malwareAttackerFile"
    "malware_url->malwareAttackerUrl"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "FireEye Alert ${alert_name} found"
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