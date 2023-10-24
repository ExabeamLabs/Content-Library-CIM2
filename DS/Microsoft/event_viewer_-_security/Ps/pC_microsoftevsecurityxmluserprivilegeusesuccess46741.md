#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-privilege-use-success-4674-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<Data Name"""
  """<EventID>4674</EventID>"""
  """<Event xmlns"""
]
Fields = [
  """<TimeCreated SystemTime[\\\/]*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Keywords>({result}.+?)</Keywords>"""
  """<Computer>({dest_host}({host}[\w.\-]+))</Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """({event_code}4674)"""
  """<Data Name[\\\/]*=('|")SubjectUserSid('|")>\s*({user_sid}[^<]+)</Data>"""
  """<Data Name[\\\/]*=('|")SubjectUserName('|")>({user}[\w\.\-]{1,40}\$?)</Data>"""
  """<Data Name[\\\/]*=('|")SubjectDomainName('|")>({domain}[^<]+?)</Data>"""
  """<Data Name[\\\/]*=('|")SubjectLogonId('|")>({login_id}[^<]+?)</Data>"""
  """<Data Name[\\\/]*=('|")ObjectServer('|")>(-|({object_server}[^<]+?))</Data>"""
  """<Data Name[\\\/]*=('|")PrivilegeList('|")>({privileges}[^<]+?)</Data>"""
  """<Data Name[\\\/]*=('|")ProcessName('|")>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))</Data>"""
  """Object Type:\s*[\\rnt]*(?:-|({object_type}[^:]+?))[\\rnt\s]*Object Name:""",
  """Desired Access:\s*[\\rnt]*({access}[^:]+?)[\\rnt\s]*Privileges:"""
  """({event_name}An operation was attempted on a privileged object)"""
  """Object Name:\s*[\\rnt]*(?:|-|({object}[^<>]+?))[\\rnt\s]*Object Handle""",
  """Logon ID:\s*[\\rnt]*({login_id}[^:]+?)[\\rnt\s]*Object:""",
  """Account Domain:\s*((\\)[rnt])*({domain}[^:]+?)((\\)[rnt])*\s*Logon ID:"""
  """Creator Process ID:((\\)[rnt])*({process_id}.+?)((\\)[rnt])*Creator"""
]
ParserVersion = "v1.0.0"


}
```