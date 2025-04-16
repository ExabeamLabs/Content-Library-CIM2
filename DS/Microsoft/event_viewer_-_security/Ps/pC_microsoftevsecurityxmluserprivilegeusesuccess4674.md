#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-use-success-4674"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
  """<EventID>4674</EventID>""","""<Data Name""","""SubjectUserName""","""<Message>An operation was attempted on a privileged object"""
]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
  """<Keywords>({result}[^<]+)<"""
  """<Computer>({dest_host}({host}[\w.\-]+))<"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """({event_code}4674)"""
  """<Data Name\\*=('|")SubjectUserSid('|")>\s*(({domain}[^\\<]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
  """<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))<"""
  """<Data Name\\*=('|")SubjectDomainName('|")>({src_domain}[^<]+?)<"""
  """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+?)<"""
  """<Data Name\\*=('|")ObjectServer('|")>(-|({object_server}[^<]+?))<"""
  """<Data Name\\*=('|")PrivilegeList('|")>({privileges}[^<]+?)<"""
  """<Data Name\\*=('|")ProcessName('|")>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))<"""
  """({event_name}An operation was attempted on a privileged object)"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = ["src_domain->domain", "src_user->user"]
ParserVersion = "v1.0.0"


}
```