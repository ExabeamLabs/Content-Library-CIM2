#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-file-success-4663-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """An attempt was made to access an object."""
  """Microsoft-Windows-Security-Auditing"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """Microsoft-Windows-Security-Auditing[^":=]+?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """(?i)(((audit|success)( |_)(success|audit))|information)[\s,](::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))).*Subject:"""
  """({event_code}4663)"""
  """({time}\w+\s\d+\s\d+:\d+:\d+\s\d+)"""
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))"""
  """Subject(:|=)[^:=]*?Security ID(:|=)\s*((NT AUTHORITY|([^\\=]+?))\\+)?(SYSTEM|({user_sid}[^=\s]+?))[\s;]*Account Name(:|=)\s*({user}[^\s;]+?)[\s;]*Account Domain(:|=)\s*(NT AUTHORITY|({domain}[^:=]+?))[\s;]*Logon ID(:|=)\s*({login_id}[^\s;]+)[\s;]*Object(:|=)"""
  """Object Type(:|=)\s*({file_type}[^:=]+?)[\s;]*Object Name(:|=)\s*({file_path}({file_dir}(\w:)?[^:=]+[\\\/]+)?({file_name}[^:=\\\/]+?(\.({file_ext}\w+))?))[\s;]*Handle ID(:|=)"""
  """Process Name(:|=)\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Access Request Information(:|=)"""
  """Accesses(:|=)\s*({access}[^:]+?)[\s;]*Access Mask(:|=)\s*({access_mask}\w+)"""
  """"AccessList":"({access}[^"]+?)\s*""""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectName":"(-|({file_path}({file_dir}[^"]+?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\"]+?))?)))\s*""""
  """"ObjectType":"(-|({file_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}(({process_dir}(?:[^";]+))?[\\\/]+)?({process_name}[^\\\/";]+?)))\s*""""
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
]
ParserVersion = "v1.0.0"


}
```