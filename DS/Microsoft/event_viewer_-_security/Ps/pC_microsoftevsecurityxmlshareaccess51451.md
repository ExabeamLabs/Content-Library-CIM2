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
  """<TimeCreated SystemTime='({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
  """<Computer>({host}[\w\-.]+)""",
  """<Computer>(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[\w\-.]+))""",
  """({event_code}5145)""",
  """<EventRecordID>({event_id}[^<]+)""",
  """'SubjectUserSid'>({user_sid}[^"\s<]+)<""",
  """'SubjectUserName'>({user}[^"\s<]+)<""",
  """'SubjectDomainName'>({domain}[^"\s<]+)<""",
  """'SubjectLogonId'>({login_id}[^"\s<]+)<""",
  """'ObjectType'>({file_type}[^<]+)<""",
  """'IpAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
  """'IpPort'>({src_port}\d+)""",
  """'ShareName'>(?:\\+\*\\+)?({share_name}.+?)<\/Data>""",
  """'ShareLocalPath'>(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}[^<]*?)({d_name}[^\\<]+?)))<\/Data>""",
  """'RelativeTargetName'>((|({f_parent}[^<]+?))({file_name}[^\\:<]+?(\.({file_ext}[^\\.<]+?))?))<\/Data>"""
  """'ObjectType'>({file_type}[^<]+)<""",
  """'ObjectType'>({file_type}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```