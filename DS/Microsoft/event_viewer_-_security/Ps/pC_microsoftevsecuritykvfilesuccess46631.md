#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-file-success-4663-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EVENT_NUMBER = 4663"""
  """An object was deleted"""
]
Fields = [
  """TIME_GENERATED\s*=\s*({time}\d{10})"""
  """({host}[\w\-.]+) ADAuditPlus"""
  """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
  """({event_name}An object was deleted)"""
  """OBJECT_NAME\s*=\s*(({file_path}({file_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({file_name}[^\\\/"\]]+?)))\s*\]"""
  """\sFILE_TYPE\s*=\s*\.({file_ext}\w+)\s*\]"""
  """LOGON_ID\s*=\s*({login_id}[^]]+?)\s*\]"""
  """DOMAIN\s*=\s*({domain}[^]]+?)\s*\]"""
  """ACCESSES\s*=\s*({access}[^]]+?)\s*\]"""
  """ACCESS_MASK\s*=\s*({access_mask}[^]]+?)\s*]"""
  """PROCESS_ID\s*=\s*(null|({process_id}[^]]+?))\s*\]"""
  """\WPROCESS_NAME\s*=\s*(|null|({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?)))\s*\]"""
  """USERNAME\s*=\s*(({user}[\w\.\-]{1,40}\$?))\s*\]"""
  """USER_SID\s*=\s*(({user_sid}[^]]+?))\s*\]"""
]
ParserVersion = "v1.0.0"


}
```