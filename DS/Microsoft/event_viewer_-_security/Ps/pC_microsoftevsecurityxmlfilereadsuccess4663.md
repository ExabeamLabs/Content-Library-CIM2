#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-file-read-success-4663"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<Data Name"""
  """"EventID":4663"""
  """xmlns"""
  """"Activity":"4663 - An attempt was made to access an object.""""
]
Fields = [
  """"TimeGenerated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"Computer"+:"+({host}[\w\-.]+)"""
  """"EventID"+:({event_code}\d+)"""
  """<Data Name(\\)?=(\\)?"+SubjectUserSid(\\)?"+>(?:NONE_MAPPED|({user_sid}[^<]+))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({domain}[^<]+))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+SubjectLogonId(\\)?"+>({login_id}[^<]+)<\/Data>"""
  """<Data Name(\\)?=(\\)?"+ObjectType(\\)?"+>({file_type}[^<]+)<\/Data>"""
  """<Data Name(\\)?="ObjectName">(({registry_path}\\+REGISTRY[^<]+?(\\\{({registry_key}[^\}<]+)\})?)|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?)|[^\\:<]+))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+ProcessName(\\)?"+>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/"<]+?))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+AccessList(\\)?"+>({access}.+?)\s(\\t)*"""
  """AccessMask"+:"+({access_mask}[^"]+)"""
  """<Level>({run_level}[^<]+)<"""
  """"Activity":"({event_name}[^"]+)""""
]
DupFields = [ "host->src_host", "user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```