#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4793-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4793<""", """<Provider Name""", """Microsoft-Windows-Security-Auditing""","""<Channel>Security</Channel>"""]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Task>({sub_category}[^<]+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """Provider Name\\*=('|")({provider_name}[^\"']+)""",
    """Guid\\*=('|")\{({process_guid}[^\"'\}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Data Name\\*=('|")Workstation('|")>([A-Fa-f:\d.]+|-|({src_host_windows}[^<]+?))\s*<""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "src_host_windows->src_host", "user->src_user", "domain->src_domain" ]


}
```