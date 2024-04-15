#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-file-success-4663-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """An attempt was made to access an object."""
  """Microsoft-Windows-Security-Auditing"""
  """Computer"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """TimeGenerated=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
  """Computer=({host}.*?)\s\w+="""
  """({event_code}4663)"""
  """"AccessList":"({access}[^"]+?)\s*""""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectName":"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*""""
  """"ObjectType":"(-|({file_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```