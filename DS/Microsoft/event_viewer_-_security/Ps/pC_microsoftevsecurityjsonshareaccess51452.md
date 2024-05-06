#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-share-access-5145-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss"]
Conditions = [
  """"Message":"A network share object was checked to see whether client can be granted desired access"""
  """"EventID":5145"""
  """Microsoft-Windows-Security-Auditing"""
]
Fields = [
  """({event_name}A network share object was checked to see whether client can be granted desired access)"""
  """({event_code}5145)"""
  """"hostname":"({host}[\w\-.]+)"""
  """"EventTime\\?":\s*\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
  """@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """SubjectLogonId"+:"+({login_id}[^"]+)"""
  """SubjectUserName"+:"+({user}[\w\.\-]{1,40}\$?)"""
  """SubjectDomainName"+:"+({domain}[^"]+)"""
  """IpAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """IpPort"+:"+({src_port}\d+)"""
  """SubjectUserSid"+:"+({user_sid}[^"<]+)"""
  """ObjectType"+:"+({file_type}[^"]+)"""
  """ShareName"+:"+[\\\*]*({share_name}[^"]+)"""
  """ShareLocalPath"+:"+(?:[\\\?]+)?(|({share_path}(({d_parent}.+?)\\\\)?(|({d_name}[^\\]*?)))\\?)""""
  """RelativeTargetName"+:"+({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\:"]+?(\.\s*({file_ext}[^"\\.]+?))?)""""
  """AccessList"+:"+({access}[^"]+)"""
  """Accesses:.*({access}SYNCHRONIZE|Execute|Traverse|Read|READ|WRITE_DAC|WRITE_OWNER|WriteAttributes|WriteEA|WriteData|AppendData|delete|Delete).*Access Check Results:"""
  """Access Check Results:\s*({result}-)\s"""
  """Access Check Results:.*({result}Granted|Denied)\s+by"""
  """Source Port(=|:)\s*((?-i)\\+[rnt])*({src_port}\d+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```