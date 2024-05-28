#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-13
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>13<""", """<EventRecordID>""", """Microsoft-Windows-Kernel-General""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({dest_host}({host}[\w\-.]+))<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Level>({run_level}\d+)"""
    """Guid=('|")\{({process_guid}[^"'\}]+)"""
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Provider>({provider_name}[^<]+?)</Provider>""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """<Keywords>({result}[^<]+)</Keywords>""",
  ]


}
```