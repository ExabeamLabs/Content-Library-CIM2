#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-5145-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>5145<"""
]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
  """<Computer>({host}[\w\-.]+)""",
  """<Computer>(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[\w\-.]+))""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """({event_code}5145)""",
  """<EventRecordID>({event_id}[^<]+)""",
  """('|")SubjectUserSid('|")>({user_sid}[^"\s<]+)<""",
  """('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
  """('|")SubjectDomainName('|")>({domain}[^"\s<]+)<""",
  """('|")SubjectLogonId('|")>({login_id}[^"\s<]+)<""",
  """('|")ObjectType('|")>({file_type}[^<]+)<""",
  """('|")IpAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
  """('|")IpPort('|")>({src_port}\d+)""",
  """('|")ShareName('|")>(?:[\\\*]+)?({share_name}.+?)<\/Data>""",
  """('|")ShareLocalPath('|")>(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}[^<]*?)({d_name}[^\\<]+?)))<\/Data>""",
  """('|")RelativeTargetName('|")>((|({file_dir}[^<]+?))({file_name}[^\\<]+?(\.({file_ext}[^\s\.\_\-\\\/]+?))?))<\/Data>""",
  """('|")ObjectType('|")>({file_type}[^<]+)<""",
  """('|")ObjectType('|")>({file_type}[^<]+)<"""
  """Source Port(=|:)\s*({src_port}\d+)"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```