#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-success-5140"
Vendor = "Microsoft"
Product = Event Viewer - Security
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [ """<EventID>5140</EventID>""", """<Data Name""", """ShareName""" ]
Fields = [
  """({event_name}A network share object was accessed)""",
  """<EventID>({event_code}5140)""",
  """<Computer>({host}({dest_host}[\w\-.]+))</Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<TimeCreated SystemTime(\\\/)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d*Z('|")/>""",
  """<TimeCreated SystemTime(\\\/)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")/>""",
  """<Data Name(\\\/)?=('|")SubjectLogonId('|")>({login_id}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
  """<Data Name(\\\/)?=('|")SubjectDomainName('|")>({domain}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")ObjectType('|")>({file_type}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")IpAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>""",
  """<Data Name(\\\/)?=('|")ShareName('|")>(?:[\\\*]*)?({share_name}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")ShareLocalPath('|")>(?:[\\\\/?]+)?(|({share_path}({d_parent}[^<]+?[\\\/])?({d_name}[^\\\/<]+?)?[\\\/]?))</Data>""",
  """({access}4416)""",
  """<Data Name(\\\/)?=('|")AccessList('|")>(%%)?({access}[\d\w]+)"""
  """('|")IpPort('|")>({src_port}\d+)"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```