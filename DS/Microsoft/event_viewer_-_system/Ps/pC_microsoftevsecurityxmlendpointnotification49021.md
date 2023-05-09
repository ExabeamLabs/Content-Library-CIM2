#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4902-1
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = ["""<EventID>4902<""" , """<Event xmlns""" ,"""<Provider Name""","""'Microsoft-Windows-Security-Auditing'"""]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*='({provider_name}[^\']+)""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Execution ProcessID\\*='({process_id}[^']+)""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """<Keywords>({result}[^<]+)"""
  ]


}
```