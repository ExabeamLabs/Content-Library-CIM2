#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-file-success-timestamp"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"event_id":4663,"""
  """An attempt was made to access an object"""
  """AccessList"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """"@timestamp"\s*:\s*\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """"(?:winlog\.)?computer_name\"\s*:\s*\"({host}[\w\-.]+?)""""
  """"record_number"\s*:\s*\"({event_id}\d+)"""
  """({event_code}4663)"""
  """"SubjectUserSid"\s*:\s*\"({user_sid}[^\"]+)"""
  """"SubjectUserName"\s*:\s*\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"SubjectDomainName"\s*:\s*\"({domain}[^\"]+)"""
  """"SubjectLogonId"\s*:\s*\"({login_id}[^\"]+)"""
  """"ObjectType"\s*:\s*\"({file_type}[^\"]+)"""
  """"ObjectName"\s*:\s*\"({src_file_path}[^\"]+)"""
  """"ObjectName"\s*:\s*\"[^\"]+\\({src_file_name}[^\".]+(\.({src_file_ext}[^\"\\.]+))?)\""""
  """"ObjectName"\s*:\s*\"(?:({file_dir}[^\"]+?)\\+[^\"\\]+)""""
  """"ProcessName"\s*:\s*\"({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+))""""
  """"AccessList"\s*:\s*\"({access}.+?)""""
  """Access Request Information:[rnt\\]*Access:[rnt\\]*({access}.*)[rnt\\]*Access Mask:[rnt\\]*({access_mask}.+?)\s*(\"|$)"""
]
DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
ParserVersion = "v1.0.0"


}
```