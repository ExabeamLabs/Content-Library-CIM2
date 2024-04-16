#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4876
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4876</EventID>""", """<Data Name""", """'Microsoft-Windows-Security-Auditing'""" ]
  Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)('|")"""
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
  """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
  """<EventID>({event_code}\d+)""",
  """<Task>({sub_category}[^<]+)""",
  """<Keywords>({result}[^<]+)""",
  """Provider Name\\*='({provider_name}[^\']+)""",
  """Guid\\*='\{({process_guid}[^\'\}]+)""",
  """<Execution ProcessID(\\)?='({process_id}[^']+)""",
  """ThreadID(\\)?='({thread_id}\d+)""",
  """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
  """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[\w\.\-]{1,40}\$?)</Data>""",
  """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
  """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>"""
  """<Level>({run_level}[^<]+)<"""
	]


}
```