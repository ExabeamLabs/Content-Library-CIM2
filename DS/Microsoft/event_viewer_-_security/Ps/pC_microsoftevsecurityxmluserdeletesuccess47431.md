#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-delete-success-4743-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ParserVersion = v1.0.0
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [ """<EventID>4743</EventID>""" ,"""Computer Account Management""" ,"""<Provider Name""","""'Microsoft-Windows-Security-Auditing"""]
Fields = [
  """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
  """<Computer>({dest_host}({host}[^<]+))</Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
  """<EventID>({event_code}\d+)""",
  """<Task>({sub_category}[^<]+)""",
  """<Keywords>({result}[^<]+)""",
  """Provider Name\\*='({provider_name}[^\']+)""",
  """Guid\\*='\{({process_guid}[^\'\}]+)""",
  """<Execution ProcessID(\\)?='({process_id}[^']+)""",
  """ThreadID(\\)?='({thread_id}\d+)""",
  """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
  """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>""",
  """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
  """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
  """<Data Name[^<>]+?TargetDomainName[^<>]+?>({dest_domain}[^<>]+?)<\Data>""",
  """<Data Name[^<>]+?TargetUserName[^<>]+?>({dest_user}[^<>]+?)</Data>"""
]


}
```