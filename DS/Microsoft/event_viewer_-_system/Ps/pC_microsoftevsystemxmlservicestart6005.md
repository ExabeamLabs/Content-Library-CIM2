#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-service-start-6005
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """>6005<""", """The Event log service was started""" ]
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
  DupFields = [ "host->src_host" ]


}
```