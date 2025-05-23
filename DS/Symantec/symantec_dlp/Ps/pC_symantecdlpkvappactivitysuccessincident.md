#### Parser Content
```Java
{
Name = "symantec-dlp-kv-app-activity-success-incident"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd, yyyy hh:mm:ss a","MMM dd HH:mm:ss"]
occured_timeFormat = ["MMM dd, yyyy HH:mm:ss a"]
ParserVersion = "v1.0.0"
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
  """\s*({time}\w+\s*\d?\d\s\d+:\d+:\d+)\s"""
  """({host}[\w\.-]+)\s+incident_id"""
  """[\s,]incident_id="+({alert_id}\d+)"""
  """[\s,]blocked="+(None|({action}[^"]+?))""""
  """[\s,]policy="+({alert_name}[^"]+?)""""
  """[\s,]occurred_on=\\*"+({occured_time}\w+ \d+, \d+ \d+:\d+:\d+ \w+)\\*""""
  """[\s,]reported_on="+({time}\w+ \d+, \d+ \d+:\d+:\d+ \w+)""""
  """[\s,]policy="+({alert_type}[^"]+?)""""
  """[\s,]rules=(?:"+)?\s*({alert_type}[^="]+?)\s*(?:"+)?,\s\w+="""
  """[\s,]severity="+({alert_severity}[^"]+?)""""
  """[\s,]sender="+\s*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """,\sendpoint_username="+\s*(?:N\/A|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """[\s,]sender="+\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """,\smachine_ip="+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*",\s"""
  """,\sdestination_ip="+(?:N\/A|null\s*|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s*"*,\s"""
  """[\s,]recipients="+\s*(?:N\/A|Unknown|({target}[^",]+?))"*,"""
  """[\s,]recipients="+\s*(N\/A|({url}(\w+:\/+)?({web_domain}[^\\\/"@]+)[^\s@]*)(?::|"|\/))"""
  """[\s,]recipients="+\s*({protocol}\w+):\/\/"""
  """[\s,]subject="+(?:N\/A|({additional_info}(?:[^",]|"")+?))\s*"*,"""
  """,\sfile_name="+(?:N\/A|({file_name}[^",]+?\.({file_ext}[^"]+)))\s*"*,"""
  """,\sattachment_filename="(([^"]+\\)?({file_name}[^"]+\.({file_ext}[a-zA-Z]{2,})))\s*","""
  """,\sendpoint_machine="+(?:N\/A|({device_id}[^",]+?))\s*"*,\s"""
  """\sZID="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"*,"""
]


}
```