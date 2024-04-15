#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-privilege-use-success-4674-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """An operation was attempted on a privileged object"""
  """Computer"""
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)"""
  """TimeGenerated=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
  """Type\s*=\s*"({action}[^";]+)""""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}[^"\s;]+)"""
  """({event_code}4674)"""
  """"Account":"((NT AUTHORITY|({domain}[^\\\s"]+))\\+)?(LOCAL SERVICE|({user}[^\\\s"]+))\s*""""
  """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectServer":"(-|({object_server}[^\s"]+))"""
  """"ObjectName":"(-|({object}[^\s"]+))"""
  """"ObjectType":"(-|({object_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```