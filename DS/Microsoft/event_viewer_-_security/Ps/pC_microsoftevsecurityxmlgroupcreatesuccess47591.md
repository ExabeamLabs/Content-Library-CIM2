#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-create-success-4759-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4759</EventID>""", """<Event xmlns""", """<Provider Name""","""Microsoft-Windows-Security-Auditing""" , """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'\}]+)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Execution ProcessID\\*=('|")({process_id}[^"']+)""",
    """ThreadID\\*=('|")({thread_id}[^'"]+)""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({src_domain}({domain}[^<>]+?))</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?TargetDomainName[^<>]+?>({group_domain}[^<>]+?)<\Data>""",
    """<Data Name[^<>]+?TargetUserName[^<>]+?>({group_name}[^<>]+?)</Data>"""
    """<Level>({run_level}[^<]+)<"""
   ]


}
```