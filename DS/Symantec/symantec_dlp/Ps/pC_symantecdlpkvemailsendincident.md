#### Parser Content
```Java
{
Name = symantec-dlp-kv-email-send-incident
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
occured_timeFormat = ["MMM dd, yyyy HH:mm:ss a"]
Conditions = [
  """incident_id=""""
  """, blocked=""""
  """, policy=""""
  """, recipients=""""
  """, sender=""""
  """, severity=""""
  """, subject=""""
]
Fields = [
  """({host}[\w\.-]+)\s+incident_id"""
  """[\s,]incident_id="+({alert_id}\d+)"""
  """[\s,]blocked="+(None|({action}[^"]+?))""""
  """[\s,]policy="+({alert_name}[^"]+?)""""
  """[\s,]occurred_on=\\*"+({occured_time}\w+ \d+, \d+ \d+:\d+:\d+ \w+)\\*""""
  """[\s,]reported_on="+({reported_time}[^"]+?)""""
  """[\s,]policy="+({alert_type}[^"]+?)""""
  """[\s,]rules=(?:"+)?\s*({alert_type}[^="]+?)\s*(?:"+)?,\s\w+="""
  """[\s,]severity="+({alert_severity}[^"]+?)""""
  """[\s,]sender="+\s*({src_email_address}[^\s"@,]+@[^\s"@,]+?)""""
  """,\sendpoint_username="+\s*(?:N\/A|(({domain}[^\\]+)\\+)?({user}[^"\\]+))"""
  """[\s,]sender="+\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """,\smachine_ip="+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*",\s"""
  """,\sdestination_ip="+(?:N\/A|null\s*|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s*"*,\s"""
  """[\s,]recipients="+\s*(?:N\/A|Unknown|({target}[^",]+?))"*,"""
  """[\s,]recipients="+\s*(N\/A|({email_recipients}(?:({dest_email_address}[^\s"@,]+@[^\s@",]+?))(?:\s*,\s*[^\s"@,]+@[^\s@",]+?\s*?)*)\s*"*,)"""
  """[\s,]recipients="+\s*(N\/A|({url}(\w+:\/+)?({web_domain}[^\\\/]+)[^\s]+)(?::|"|\/))"""
  """[\s,]recipients="+\s*({protocol}\w+):\/\/"""
  """,\sprotocol="+(?:N\/A|({protocol}[^",]+?))\s*"*,"""
  """[\s,]subject="+(?:N\/A|({additional_info}(?:[^",]|"")+?))\s*"*,"""
  """,\sfile_name="+(?:N\/A|({file_name}[^",]+?))\s*"*,"""
  """,\sattachment_filename="+(?:N\/A|({file_name}[^.",]+?(?:\.({file_ext}[^",]+?))?))\s*"*,"""
  """,\sendpoint_machine="+(?:N\/A|({device_id}[^",]+?))\s*"*,\s"""
  """\sZID="+({user}[^",\s]+?)"*,"""
]
DupFields = [
  "additional_info->email_subject"
  "alert_id->message_id"
  "file_name->email_attachment"
  "device_id->src_host"
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
    "src_ip->dlpDeviceName"
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
      ]
    

}
```