#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-file-success-4663-4"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """An attempt was made to access an object."""
  """Computer"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
  """(?i)(((audit|success)( |_)(success|audit))|information)[\s,]({dest_host}({host}[\w\-.]+))\s+.*Subject:"""
  """({dest_host}({host}[\w\-.]+))\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))"""
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
  """Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s|;)"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """({event_code}4663)"""
  """Subject(:|=).*?Security ID(:|=)\s*({user_sid}.+?)[\s;]*Account Name(:|=)\s*({user}[\w\.\-]{1,40}\$?)[\s;]*Account Domain(:|=)\s*(NT AUTHORITY|({domain}.+?))[\s;]*Logon ID(:|=)\s*({login_id}[^\s;]+)[\s;]*Object(:|=)"""
  """Object(:|=).*?Object Type(:|=)\s*({file_type}.+?)[\s;]*Object Name(:|=)\s*({file_path}({file_dir}.*?)(|({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\]+?))?)))[\s;]*Handle ID(:|=)""",
  """Process Name(:|=)\s*(?:|({process_path}.+?))[\s;]*Access Request Information(:|=)"""
  """Process Name(:|=).*\\({process_name}[^\\;]+?)[\s;]*Access Request Information(:|=)"""
  """Process Name(:|=)\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Access Request Information(:|=)"""
  """Accesses(:|=)\s*({access}.+?)[\s;]*Access Mask(:|=)\s*({access_mask}\w+)"""
  """"AccessList":"({access}[^"]+?)\s*""""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectName":"(-|({src_file_path}({file_dir}.*?)({src_file_name}[^\\\/;]+?(\.({src_file_ext}[^\.;]+?))?)))\s*"""
  """"ObjectType":"(-|({file_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
]
ParserVersion = "v1.0.0"


}
```