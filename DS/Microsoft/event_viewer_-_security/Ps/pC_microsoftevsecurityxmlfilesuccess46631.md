#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-success-4663-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4663</EventID>""","""<Data Name""",""""SubjectUserSid""""
]
Fields = [
  """<TimeCreated SystemTime\\*="({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """<Computer>([^<>]+?[\\\/]+)?({src_host}({host}[\w\-.]+))</Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<EventID>({event_code}[^<]+)</EventID>"""
  """<Data Name\\*="SubjectUserSid">(?:NONE_MAPPED|({user_sid}[^<]+))<"""
  """<Data Name\\*="SubjectUserName">(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
  """<Data Name\\*="SubjectDomainName">(?=\w)({domain}[^<]+)<"""
  """<Data Name\\*="SubjectLogonId">({login_id}[^<]+)<"""
  """<Data Name\\*="ObjectType">({file_type}[^<]+)<"""
  """<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?(\\\{({registry_key}[^\}<]+)\})?)|({src_file_path}[^<]+))<"""
  """<Data Name\\*="ObjectName">(?!\\+REGISTRY)[^<]+[\\\/]+({src_file_name}(?:[^<\\\/:]+?)(\.({src_file_ext}\w+))?|[^\\:<]+)<"""
  """<Data Name\\*="ObjectName">(?!\\+REGISTRY)({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)<"""
  """<Data Name\\*="ProcessName">({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"<]+?))<"""
  """<Data Name\\*="AccessList">([^\d\w]+)?({access}[\d\w]+)"""
  """<Data Name\\*="AccessMask">({access_mask}[^<\s"]+)"""
  """Accesses:\s*({access}[^:]+?)\s*Access Mask:"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```