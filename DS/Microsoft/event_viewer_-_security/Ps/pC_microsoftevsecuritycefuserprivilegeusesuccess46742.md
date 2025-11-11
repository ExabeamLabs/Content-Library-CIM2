#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-4674-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<Data Name"""
  """"EventID":4674"""
  """xmlns"""
  """"Activity":"4674 - An operation was attempted on a privileged object.""""
]
Fields = [
  """TimeGenerated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Keywords>({result}.+?)</Keywords>"""
  """Computer"+:"+({dest_host}({host}[\w\-.]+))"""
  """({event_code}4674)"""
  """<Data Name(\\)?=(\\)?"+SubjectUserSid(\\)?"+>(?:NONE_MAPPED|({user_sid}[^<]+))"""
  """<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<\/Data>"""
  """<Data Name(\\)?=(\\)?"+SubjectLogonId(\\)?"+>({login_id}[^<]+)<\/Data>"""
  """<Data Name(\\)?=(\\)?"+ObjectServer(\\)?"+>(-|({object_server}[^<]+))"""
  """<Data Name(\\)?=(\\)?"+PrivilegeList(\\)?"+>({privileges}[^<]+)"""
  """<Data Name(\\)?=(\\)?"+ProcessName(\\)?"+>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))<\/Data>"""
  """"Activity".+?({event_name}An operation was attempted on a privileged object)"""
  """<Data Name(\\)?=(\\)?"+ProcessId(\\)?"+>({process_id}[^<]+)<\/Data>"""
  """<Data Name(\\)?=(\\)?"+ObjectType(\\)?"+>(-|({object_type}[^<]+))"""
  """<Data Name(\\)?=(\\)?"+ObjectName(\\)?"+>(-|({object}[^<]+))"""
]
ParserVersion = "v1.0.0"


}
```