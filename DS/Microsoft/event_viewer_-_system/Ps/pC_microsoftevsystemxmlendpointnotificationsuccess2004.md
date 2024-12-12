#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-success-2004
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>2004</EventID>""", """<Provider Name =""", """<Channel>System<""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)"""
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[\w\-.]+)"""
    """<Process_1><Name>({process_name}[^<]+)</Name>"""
    """<Provider Name\\*=('|")({provider_name}[^'"]+)('|")"""
    """<Keywords>({result}[^<]+)<\/Keywords>"""
    """<EventRecordID>({event_id}.+?)<\/EventRecordID>"""
    """<Execution ProcessID\\*=('|")({process_id}[^'"]+)"""
    """ThreadID\\*=('|")({thread_id}[^'"]+)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```