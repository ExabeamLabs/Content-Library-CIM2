#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4872
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4872</EventID>""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)('|")"""
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
  """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
  """<EventID>({event_code}\d+)""",
  """<Message>({event_name}[^<\.]+)""",
  """<Task>({sub_category}[^<]+)""",
  """<Keywords>({result}[^<]+)""",
  """Provider Name\\*='({provider_name}[^\']+)""",
  """Guid\\*='\{({process_guid}[^\'\}]+)""",
  """<Execution ProcessID(\\)?='({process_id}[^']+)""",
  """ThreadID(\\)?='({thread_id}\d+)"""
  """<Level>({run_level}[^<]+)<"""
  ]
 

}
```