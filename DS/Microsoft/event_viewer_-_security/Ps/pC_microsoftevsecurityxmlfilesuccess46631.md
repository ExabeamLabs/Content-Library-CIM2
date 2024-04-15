#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-success-4663-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4663</EventID>"""
  """<Data Name ="SubjectUserSid""""
]
Fields = [
  """<TimeCreated SystemTime="({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}[^<]+)</Computer>"""
  """<EventID>({event_code}[^<]+)</EventID>"""
  """<Data Name ="SubjectUserSid">(?:NONE_MAPPED|({user_sid}[^<]+))<"""
  """<Data Name ="SubjectUserName">(?=\w)({user}[^<]+)<"""
  """<Data Name ="SubjectDomainName">(?=\w)({domain}[^<]+)<"""
  """<Data Name ="SubjectLogonId">({login_id}[^<]+)<"""
  """<Data Name ="ObjectType">({file_type}[^<]+)<"""
  """<Data Name ="ObjectName">({src_file_path}[^<]+)<"""
  """<Data Name ="ObjectName">[^<]+[\\\/]+({src_file_name}(?:[^<\\\/:]+?)(\.({src_file_ext}\w+))?|[^\\:<]+)<"""
  """<Data Name ="ObjectName">({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)<"""
  """<Data Name ="ProcessName">({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"<]+?))<"""
  """<Data Name ="AccessList">([^\d\w]+)?({access}[\d\w]+)"""
  """<Data Name ="AccessMask">({access_mask}[^<\s"]+)"""
  """Accesses:\s*({access}[^:]+?)\s*Access Mask:"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```