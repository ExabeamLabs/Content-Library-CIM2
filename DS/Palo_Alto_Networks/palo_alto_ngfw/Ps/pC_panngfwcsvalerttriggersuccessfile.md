#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-file"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """,THREAT,file,"""
]
Fields = [
  """THREAT,[^,]+,[^,]+,({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z),"""
  """THREAT,file,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """THREAT,([^,]*,){3}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,"""
  """THREAT,file,((""|".*?[^"]"|[^,]*),){25}({action}[^,]+)"""
  """THREAT,file,((""|".*?[^"]"|[^,]*),){54}({host}[\w\-\.]+)(,|$)"""
  """:\d\d:\d\d(([+-]\d\d:\d\d)|(\.\d+Z))?\s+({host}[\w.-]+)\s"""
  """THREAT,file,([^,]*,){8}(|({dest_domain}[^\\,]+))\\?(|({dest_user}[^\\,]+))(,|$)"""
  """THREAT,file,([^,]*,){7}(?:({user}[^@,]+)@({domain}[^\.,]+\.[^,]+)|(?:|({=domain}[^\\,]+))\\?(?:|({=user}[^\\,]+)))(,|$)"""
  """THREAT,file,([^,]*,){6}({alert_name}[^,]+)"""
  """({alert_type}file)"""
  """THREAT,file,((""|".*?[^"]"|[^,]*),){31}({alert_id}\d+)(,|$)"""
  """THREAT,file,((""|".*?[^"]"|[^,]*),){26}"?(?:|({file_name}[^.",]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*("|,)"""
  """THREAT,file,([^,]*,){26}"?(?:|({file_name}[^.",]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*("|,)"""
  """THREAT,file,((""|"[^"]+?"|[^,]*),){26}("(?:|({file_name}[^."]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*",|("")?,)"""
  """THREAT,file,([^,]*,){26}"*(|({file_name}[^\n]+?(\.({file_ext}[^",\-\.\_\/]+?))?))\s*\/?"*\/?,\w+"""  
  """THREAT,file,((""|"[^"]+?"|[^,]*),){29}({alert_severity}[^,]+)(,|$)"""
  """THREAT,file,([^,]*,){27}({additional_info}[^,]+)"""
]
DupFields = ["alert_name->rule", "user->src_user"]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
    "src_ip->malwareVictimHost"
    "alert_type->malwareCategory"
    "file_name->malwareAttackerFile"
    "dest_ip->malwareAttackerIp"
    "action->description"
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
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