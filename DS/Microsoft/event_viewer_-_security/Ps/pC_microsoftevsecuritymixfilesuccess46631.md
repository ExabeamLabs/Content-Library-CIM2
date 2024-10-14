#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-file-success-4663-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [
  """An attempt was made to access an object."""
  """Microsoft-Windows-Security-Auditing"""
  """Computer"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """TimeGenerated=({time}\d{10})"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{7,9}Z)""",
  """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """Computer=({host}[\w\-.]*?)\s*\w+="""
  """({event_code}4663)"""
  """"AccessList":"({access}[^"]+?)\s*""""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectName":"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*""""
  """"ObjectType":"(-|({file_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  """<TimeCreated SystemTime=("|')({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}[\w\-.]+)<"""
  """<EventID>({event_code}[^<]+)<"""
  """<Data Name =("|')SubjectUserSid("|')>(?:NONE_MAPPED|({user_sid}[^<]+))<"""
  """<Data Name =("|')SubjectUserName("|')>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
  """<Data Name =("|')SubjectDomainName("|')>(?=\w)({domain}[^<]+)<"""
  """<Data Name =("|')SubjectLogonId("|')>({login_id}[^<]+)<"""
  """<Data Name =("|')ObjectType("|')>({file_type}[^<]+)<"""
  """<Data Name =("|')ObjectName("|')>({src_file_path}[^<]+)<"""
  """<Data Name =("|')ObjectName("|')>[^<]+[\\\/]+({src_file_name}(?:[^<\\\/:]+?)(\.({src_file_ext}\w+))?|[^\\:<]+)<"""
  """<Data Name =("|')ObjectName("|')>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)<"""
  """<Data Name =("|')ProcessName("|')>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"'<]+?))<"""
  """<Data Name =("|')AccessList("|')>\s*({access}[^<]+?)\s*<"""
  """<Data Name =("|')AccessMask("|')>({access_mask}[^<\s"']+)"""
  """Accesses:\s*({access}[^:]+?)\s*Access Mask:"""
]
DupFields = [
  "host->src_host"
]
ParserVersion = "v1.0.0"


}
```