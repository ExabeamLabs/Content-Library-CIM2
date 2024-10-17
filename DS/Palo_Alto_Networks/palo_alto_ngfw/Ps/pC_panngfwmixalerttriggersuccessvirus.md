#### Parser Content
```Java
{
Name = "pan-ngfw-mix-alert-trigger-success-virus"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,virus,"""
]
Fields = [
  """"host":\{[^=]*?"name":"({host}[^"]+)"[^=]*?\}"""
  """({host}[\w\-\.]+)\s+\d+,[^,]*,[^,]*,THREAT,virus,"""
  """,THREAT,([^,]*,){55}(|({host}[^,]+)),"""
  """,THREAT(,[^,]*){40},("[^"]*",)([^,]*,){3}("[^"]*",){5}([^,]*,){6}({host}[^,]+)."""
  """THREAT,({alert_type}virus),\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),([^,]*,){3}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^\\,]+)\\+)?(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))),(({dest_domain}[^\\,]+)\\+)?(?:|({dest_user}[^,]+)),"""
  """,THREAT,([^,]*,){26}({action}[^,]+),"""
  """,THREAT,([^,]*,){27}\\?"(|({malware_url}[^\s]+?))\\?","""
  """THREAT,virus,((""|".*?[^"]"|[^,]*),){26}\\?"?(?:|({file_name}[^.",]+?(\.({file_ext}[^,."?_]{1,5}?))?))\s*\\?("|,)"""
  """THREAT,virus,([^,]*,){26}"?(?:|({file_name}[^.",]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*("|,)"""
  """THREAT,virus,((""|"[^"]+?"|[^,]*),){26}("(?:|({file_name}[^."]+?(\.({file_ext}[^,."?_]{1,5}))?))\s*",|("")?,)"""
  """THREAT,virus,([^,]*,){26}"*(|({file_name}[^\n]+?(\.({file_ext}[^",\-\.\_\/]+?))?))\s*\/?"*\/?,"""
  """,THREAT,.+?,\\?"[^"]*",({alert_name}[^,]+),"""
  """,THREAT,.+?,\\?"[^"]*",[^,]*,"?(unknown|({category}[^,"]+))"?,"""
  """,THREAT,([^,]*,){29}({category}[^,]+),"""
  """THREAT,virus,.+?,\\?"[^"]*",([^,]*,){2}({alert_severity}[^,]+),"""
  """THREAT,virus,.+?,\\?"[^"]*",([^,]*,){4}({alert_id}[^,]+),"""
  """,({alert_severity}(?i)(low|medium|high|critical|informational)),({direction}[^,]*),([^,]+,){3}({src_location}[^\d,]+)?"""
  """THREAT,virus,(("[^"]+?"|[^,]*),){64}({threat_category}[^,]+),"""
  """,THREAT,([^,]*,){28}(\d+|({alert_name}[^\(,]+?))\(({alert_id}\d+)?""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
  """,THREAT,([^,]*,){10}({alert_source}[^,]+?),"""
  """({event_category}THREAT)"""
  """,THREAT,({alert_type}[^,]+),([^,]*,){2}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),"""
  """,THREAT,([^,]*,){20}(|({src_port}\d+)),(|({dest_port}\d+)),(|({src_translated_port}\d+)),(|({dest_translated_port}\d+)),"""
  """,THREAT,([^,]*,){55}(|({device_name}[^,]+))"""
  """({serial_num}[^,]+),THREAT,"""
  """,THREAT,([^,]*,){55}(|({host}[^,]+))"""
  ]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "src_ip->malwareVictimHost"
    "alert_id->sourceId"
    "alert_type->malwareCategory"
    "malware_url->malwareAttackerUrl"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
      ]
    

}
```