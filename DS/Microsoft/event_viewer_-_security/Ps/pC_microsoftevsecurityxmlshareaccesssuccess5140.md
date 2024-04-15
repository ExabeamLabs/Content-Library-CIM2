#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-success-5140"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [ """<EventID>5140</EventID>""", """<Data Name""", """'ShareName'>""" ]
Fields = [
  """<EventID>({event_code}5140)""",
  """<Computer>({host}({dest_host}[\w-]+)[^<]*)</Computer>""",
  """<TimeCreated SystemTime(\\\/)?='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d*Z'/>""",
  """<Data Name(\\\/)?='SubjectLogonId'>({login_id}[^<]+?)</Data>""",
  """<Data Name(\\\/)?='SubjectUserName'>(-|({user}[^<]+?))</Data>""",
  """<Data Name(\\\/)?='SubjectDomainName'>({domain}[^<]+?)</Data>""",
  """<Data Name(\\\/)?='ObjectType'>({file_type}[^<]+?)</Data>""",
  """<Data Name(\\\/)?='IpAddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>""",
  """<Data Name(\\\/)?='ShareName'>(?:[\\\*]*)?({share_name}[^<]+?)</Data>""",
  """<Data Name(\\\/)?='ShareLocalPath'>(?:[\\\\/?]+)?(|({share_path}({d_parent}[^<]+?[\\\/])?({d_name}[^\\\/<]+?)?[\\\/]?))</Data>""",
  """({access}4416)""",
  """<Data Name(\\\/)?='AccessList'>(%%)?({access}[\d\w]+)"""
]
ParserVersion = "v1.0.0"


}
```