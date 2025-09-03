#### Parser Content
```Java
{
Name = "fireeye-networksecurity-cef-alert-trigger-success-trellix"
Vendor = "Trellix"
Product = "Trellix Network Security (NX)"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [ """CEF:""" , """|Trellix|""" , """|MPS|""" ]
Fields = [
  """\Wrt=({time}[a-zA-Z]{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
  """externalId=({alert_id}\d+)""",
  """\|Trellix\|([^\|]+\|){3}({alert_type}[^\|]+)\|({alert_severity}[^\|]+)\|""",
  """\|Trellix\|([^\|]+\|){3}({alert_name}[^\|]+)\|""",
  """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """shost=({dest_host}[\w\-.]+)""",
  """(filePath|fname)=(?:({malware_url}[^\s.]+\.[^\/\s]+\/[^=]+?)|({malware_file_name}[^=]+?))\s\w+=""",
  """cs1Label=sname cs1=({alert_name}[^=]+?)\s\w+=""",  
  """cs5Label=cncHost cs5=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))""",
  """request=({malware_url}[^\s]+)""",
  """dst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """dhost=({src_host}[\w\-.]+)""",
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^\s]+)?\s+cn1Label""",
  """dvc=(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-.]+))""",
  """dvchost=({host}[\w\-.]+)""",
  """act=({action}[^=]+?)\s+\w+=""",
  """categoryOutcome=(\/)?({result}[^\s]+)"""
  """CEF:([^\|]*\|){4}({operation}[^\|]+)""",
  """request=({resource}[^\s=]+)\s*(\w+=|$)"""
  """suser=suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """act=({category}[^=]+)\s+\w+="""
  """msg=({additional_info}[^=]+)\s+\w+=""",
  """\|Trellix\|({app}[^\|]+)\|"""
]
DupFields = [ "resource->object", "operation->event_name" ]
ParserVersion = "v1.0.0"


}
```