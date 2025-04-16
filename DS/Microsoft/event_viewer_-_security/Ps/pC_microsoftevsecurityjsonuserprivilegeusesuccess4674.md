#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-4674"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
Conditions = [
  """"EventID":4674"""
  """An operation was attempted on a privileged object"""
]
Fields = [
  """"EventTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """"EventID"*:({event_code}\d+)"""
  """({event_name}An operation was attempted on a privileged object)"""
  """"(Hostname|Computer)"*:"*({host}[^"]+)"""
  """EventType"*:"*({result}[^"]+)"""
  """ProcessName"*:"*(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
  """"SubjectUserSid"*:"*(SYSTEM|({user_sid}[^"]+))"""
  """"SubjectUserName"*:"*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"SubjectDomainName"*:"*({domain}[^"]+)"""
  """"SubjectLogonId"*:"*({login_id}[^"]+)"""
  """"ProcessID"*:({process_id}[^,"]+)"""
  """"HandleId"*:"*({object_id}[^"]+)"""
  """"ObjectType"*:"*(-|({object_type}[^"]+))"""
  """"ObjectName"*:"*(-|({object}[^"]+))"""
  """"ObjectServer":"(-|({object_server}[^\s"]+))"""
  """AccessMask"*:"*(-|({access}[^"]+))"""
  """PrivilegeList"*:"*(-|({privileges}[^"]+))"""
  """"Category"*:"*({category}[^"]+)"""
  """"Opcode"*:"*({severity}[^"]+)"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```