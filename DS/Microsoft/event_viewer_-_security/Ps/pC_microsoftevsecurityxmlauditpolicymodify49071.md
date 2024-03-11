#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-audit-policy-modify-4907-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = ["""<EventID>4907<""" ,"""Audit Policy Change""" ,"""<Provider Name ='Microsoft-Windows-Security-Auditing'""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<""",
    """Guid='\{({process_guid}[^\'\}]+)""",
    """<Execution ProcessID(\\)?='({process_id}[^']+)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """ThreadID(\\)?='({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name ='({provider_name}[^\']+)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Data Name ='ProcessName'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/\"]+?))<\/Data>""",
    """<Data Name ='SubjectUserName'>(-|({user}[^<]+))</Data>""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)<\/Data>""",
    """<Data Name ='SubjectDomainName'>(-|({domain}[^<]+))</Data>""",
    """<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>"""
  ]


}
```