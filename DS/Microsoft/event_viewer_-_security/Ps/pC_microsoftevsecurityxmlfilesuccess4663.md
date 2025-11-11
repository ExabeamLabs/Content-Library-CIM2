#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-success-4663"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
  """<EventID>4663</EventID>""","""<Data Name""","""'SubjectUserSid'"""
]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """<Computer>({src_host}({host}[\w\-.]+))<"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<EventID>({event_code}[^<]+)<"""
  """<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))<"""
  """<Data Name\\*=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<"""
  """<Data Name\\*=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))<"""
  """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
  """<Data Name\\*=('|")ObjectType('|")>({file_type}[^<]+)<"""
  """<Data Name\\*=('|")ObjectName('|")>(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^<\\\/]+))|({file_path}[^<]+))<"""
  """<Data Name\\*=('|")ObjectName('|")>(?!\\+REGISTRY)[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)<"""
  """<Data Name\\*=('|")ObjectName('|")>(?!\\+REGISTRY)({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)<"""
  """<Data Name\\*=('|")ProcessName('|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"<]+?))<"""
  """<Data Name\\*=('|")AccessList('|")>([^\d\w]+)?({access}[\d\w]+)"""
  """<Data Name\\*=('|")AccessMask('|")>({access_mask}[^<\s"]+)"""
  """Accesses:\s*(\\r|\\n|\\t)*({access}[^:]+?)\s*(\\r|\\n|\\t)*Access Mask:"""
  """({event_name}An attempt was made to access an object)"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```