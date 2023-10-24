#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4877
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4877</EventID>""", """<Message>Certificate Services backup completed""", """'Microsoft-Windows-Security-Auditing'""" ]
  Fields = [
  """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)'"""
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
	]


}
```