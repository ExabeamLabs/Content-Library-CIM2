#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4985-1
  Product = Event Viewer - System
  Vendor = Microsoft
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4985<""", """<Provider Name""","""'Microsoft-Windows-Security-Auditing'""" , """<Data Name""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """ThreadID(\\)?='({thread_id}\d+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[\w\.\-]{1,40}\$?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessId[^<>]+?>({process_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>"""
	]


}
```