#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-service-create-success-5478-1
Vendor = Microsoft
Product = Event Viewer - Security
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>5478<""", """<Provider Name""", """Microsoft-Windows-Security-Auditing""" ]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<Computer>({dest_host}({host}[\w\-.]+))""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<Task>({sub_category}[^<]+)""",
  """<Keywords>({result}[^<]+)<\/Keywords>""",
  """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
  """<Provider Name\\*=('|")Microsoft-Windows-Security-Auditing('|") Guid=('|")\{({process_guid}[^}]+?)\}""",
  """<Correlation ActivityID\\*=('|")\{({activity_id}[^\}'"]+)""",
  """<Execution ProcessID\\*=('|")({process_id}[^'"]+)""",
  """ThreadID\\*=('|")({thread_id}[^'"]+)""",
  """<Level>({run_level}[^<]+)<"""
]


}
```