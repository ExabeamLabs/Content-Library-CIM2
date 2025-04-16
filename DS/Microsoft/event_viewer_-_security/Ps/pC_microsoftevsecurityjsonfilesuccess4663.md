#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-4663"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"EventID":4663"""
  """"SourceModuleType":"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """"EventTime":({time}\d+)"""
  """"EventTime":\s*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""""
  """"Hostname":"({host}[\w\-.]*)"""
  """({event_code}4663)"""
  """"SubjectUserSid":"({user_sid}[^"]+)"""
  """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"SubjectDomainName":"({domain}[^"]+)"""
  """"SubjectLogonId":"({login_id}[^"]+)"""
  """"ObjectType":"({file_type}[^"]+)"""
  """"ObjectName":"({src_file_path}[^"]+)"""
  """"ObjectName"+:".*\\({src_file_name}(?:[^\\:]+(?=\.))({src_file_ext}\.[^\\:\s]+)?|[^\\:\s]+)"+,"+HandleId"""
  """"ObjectName":"+(?:({file_dir}.+?)\\+[^\\]+)","HandleId""""
  """"ProcessName":"({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+))""""
  """Access Request Information:[rnt\\]*Accesses:[rnt\\]*({access}[^:]+?)[rnt\\]*Access Mask:[rnt\\]*({access_mask}\w+)"""
]
ParserVersion = "v1.0.0"
DupFields = [ "user->src_user", "domain->src_domain" ]


}
```