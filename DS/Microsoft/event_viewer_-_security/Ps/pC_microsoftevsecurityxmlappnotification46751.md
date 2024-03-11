#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-notification-4675-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4675</EventID>""", """<Provider Name ='Microsoft-Windows-Security-Auditing'""" , """Logon"""]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Computer>({host}[^<]+)""",
    """<EventID>({event_code}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Execution ProcessID(\\)?='({process_id}[^']+)""",
    """Provider Name ='({provider_name}[^\']+)""",
    """Guid='\{({process_guid}[^\'\}]+)""",
    """ThreadID(\\)?='({thread_id}\d+)""",
    """Provider Name ='({provider_name}[^\']+)"""
  ]
  DupFields = [ "host-> dest_host" ]


}
```