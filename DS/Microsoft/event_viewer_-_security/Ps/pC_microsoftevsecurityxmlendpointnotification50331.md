#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-5033-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>5033<""" , """<Provider Name""","""Microsoft-Windows-Security-Auditing""" ,"""<Event xmlns""","""<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*='({provider_name}[^\']+)""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<EventID>({event_code}[^<]+)<""",
    """<Execution ProcessID\\*='({process_id}[^']+)""",
    """ThreadID\\*='({thread_id}[^']+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """<Keywords>({result}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```