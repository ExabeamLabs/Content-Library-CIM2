#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4755-1
  Vendor = Microsoft
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4755</EventID>""", """<Provider Name""","""Microsoft-Windows-Security-Auditing""", """<Execution ProcessID""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'\}"]+)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Data Name[^<>]+?TargetUserName[^<>]+?>({group_name}[^<]+)""",
    """<Data Name[^<>]+?TargetDomainName[^<>]+?>({group_domain}[^<]+)<""",
    """<Data Name[^<>]+?TargetSid[^<>]+?>({group_id}[^<]+)""",
    """<Data Name[^<>]+?PrivilegeList[^<>]+?>({privileges}[^<]+?)<""",   
    """<Level>({run_level}[^<]+)<"""
  ]


}
```