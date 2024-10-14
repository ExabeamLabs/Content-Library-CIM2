#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-file-success-4663-5"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss"]
Conditions = [
  """An attempt was made to access an object."""
  """Microsoft-Windows-Security-Auditing"""
  """AUDIT_SUCCESS"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """Microsoft-Windows-Security-Auditing.+?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """({host}[\w\-.]+) AUDIT_SUCCESS"""
  """({event_code}4663)"""
  """Subject(:|=).*?Security ID(:|=)\s*({user_sid}.+?)[\s;]*Account Name(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s;]*Account Domain(:|=)\s*(NT AUTHORITY|({domain}.+?))[\s;]*Logon ID(:|=)\s*({login_id}[^\s;]+)[\s;]*Object(:|=)"""
  """Object(:|=).*?Object Type(:|=)\s*({file_type}.+?)[\s;]*Object Name(:|=)\s*({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\]+?))?))[\s;]*Handle ID(:|=)"""
  """Process Name(:|=)\s*(?:|({process_path}.+?))[\s;]*Access Request Information(:|=)"""
  """Process Name(:|=).*\\({process_name}[^\\;]+?)[\s;]*Access Request Information(:|=)"""
  """Process Name(:|=)\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\";]+?)))[\s;]*Access Request Information(:|=)"""
  """Accesses(:|=)\s*({access}.+?)[\s;]*Access Mask(:|=)\s*({access_mask}\w+)"""
  """"AccessList":"({access}[^"]+?)\s*""""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectName":"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*""""
  """"ObjectType":"(-|({file_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
]
ParserVersion = "v1.0.0"


}
```