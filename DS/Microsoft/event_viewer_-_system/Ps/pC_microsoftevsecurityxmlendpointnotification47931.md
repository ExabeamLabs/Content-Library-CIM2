#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4793-1
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4793<""", """Other Account Management""" , """<Provider Name""","""'Microsoft-Windows-Security-Auditing'"""]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<Task>({sub_category}[^<]+)""",
    """ThreadID(\\)?='({thread_id}\d+)""",
    """Provider Name\\*='({provider_name}[^\']+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """<Execution ProcessID(\\)?='({process_id}[^']+)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Data Name\\*='Workstation'>([A-Fa-f:\d.]+|-|({src_host_windows}[^<]+?))\s*<""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>"""	
  ]


}
```