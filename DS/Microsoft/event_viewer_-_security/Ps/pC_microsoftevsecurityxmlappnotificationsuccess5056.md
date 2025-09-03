#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-notification-success-5056
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
  """<EventID>5056</EventID>""",
  """SubjectUserSid""",
  """SubjectUserName"""
  ]
  Fields = [
  """<EventID>({event_code}[^<]+)<\/EventID>"""
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """<Provider Name\\*=('|")({provider_name}[^'"]+)('|")"""
  """<Keywords>({result}[^<]+)<\/Keywords>"""
  """<EventRecordID>({event_id}.+?)<\/EventRecordID>"""
  """<Execution ProcessID\\*=('|")({process_id}[^'"]+)"""
  """ThreadID\\*=('|")({thread_id}[^'"]+)"""
  """<Computer>({host}[^<]+?)<"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<"""
  """<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
  """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<"""
  """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
  """<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))<"""
  """<Data Name\\*=('|")PrivilegeList('|")>({privileges}[^<]+?)<"""
  """<Message>({event_name}[^.<]+)\s*""",
  """<Level>({run_level}[^<]+)<"""
]
DupFields = ["user->src_user", "domain->src_domain"]


}
```