#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-log-disable-6006
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """>6006<""", """The Event log service was stopped""" ]
  Fields = [
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<EventRecordID>({event_id}\d+)""",
    """<Message>({event_name}[^:<\.]+)""",
    """<Keywords>({result}.+?)</Keywords>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """ThreadID='({thread_id}[^']+)""",
    """ProcessID='({process_id}\d+)""",
    """Provider Name:\s*({provider_name}.+?)\s+Algorithm Name:""",
  ]


}
```