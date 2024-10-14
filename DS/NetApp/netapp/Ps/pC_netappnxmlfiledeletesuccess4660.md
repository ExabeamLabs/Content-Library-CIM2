#### Parser Content
```Java
{
Name = "netapp-n-xml-file-delete-success-4660"
Vendor = "NetApp"
Product = "NetApp"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4660</EventID>"""
  """SubjectUserSid"""
  """NetApp-Security-Auditing"""
]
Fields = [
  """<TimeCreated SystemTime="+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>"""
  """<EventID>({event_code}[^<]+)<\/EventID>"""
  """<EventName>({event_name}[^<]+)<\/EventName>"""
  """<Result>({result}[^<]+)</Result>"""
  """<Data Name\\*=('|")*SubjectIP("|')*.*?>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
  """<Data Name\\*=('|")*SubjectUserSid('|")*>({user_sid}.+?)</Data>"""
  """<Data Name\\*=('|")*SubjectDomainName('|")*>({domain}.+?)</Data>"""
  """<Data Name\\*=('|")*SubjectUserName('|")*>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
  """<Data Name\\*=('|")*ObjectServer('|")*>({object_server}.+?)</Data>"""
  """<Data Name\\*=('|")*ObjectType('|")*>({file_type}.+?)</Data>"""
  """<Data Name\\*=('|")*ObjectName('|")*>({file_path}.+?)<\/Data>"""
  """<Data Name\\*=('|")*ObjectName('|")*>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>"""
  """<Data Name\\*=('|")*ObjectName('|")*>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>"""
  """<Data Name\\*=('|")*ProcessName('|")*>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/"<]+?))</Data>"""
  """<Data Name\\*=('|")*(HandleID|HandleId)('|")*>({object_id}.+?)</Data>"""
]
DupFields = [
  "event_name->operation"
]
ParserVersion = "v1.0.0"


}
```