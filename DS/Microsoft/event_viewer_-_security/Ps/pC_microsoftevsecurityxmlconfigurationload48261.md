#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-configuration-load-4826-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4826<""" , """<Provider Name""","""'Microsoft-Windows-Security-Auditing'""", """Other Policy Change Events"""]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*='({provider_name}[^\']+)""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Execution ProcessID\\*='({process_id}[^']+)""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>"""
	]


}
```