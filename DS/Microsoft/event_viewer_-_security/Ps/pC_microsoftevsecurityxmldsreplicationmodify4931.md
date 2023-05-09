#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-ds-replication-modify-4931
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4931<""", """Detailed Directory Service""" ,"""<Provider Name""","""'Microsoft-Windows-Security-Auditing'""" ]
  Fields = [
	"""<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
	"""<Computer>({host}[^<>]+)<""",
	"""Guid\\*='\{({process_guid}[^\'\}]+)""",
	"""<Execution ProcessID(\\)?='({process_id}[^']+)""",
	"""<EventID[^<]*?>({event_code}\d+)""",
	"""ThreadID(\\)?='({thread_id}\d+)""",
	"""<Keywords>({result}[^<]+)""",
	"""<Task>({sub_category}[^<]+)""",
	"""Provider Name\\*='({provider_name}[^\']+)""",
	"""<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
  """<Data Name\\*='DestinationDRA'>.+?CN=({dest_dra}[^<]+)""",
  """<Data Name\\*='SourceDRA'>.+?CN=({src_dra}[^<]+)"""
	]


}
```