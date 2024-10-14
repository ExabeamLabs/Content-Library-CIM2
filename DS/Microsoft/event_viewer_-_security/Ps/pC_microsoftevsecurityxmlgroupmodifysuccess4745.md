#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4745
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """<EventID>4745</EventID>""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing""" , """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """Guid\\*=('|")\{({process_guid}[^\"'\}]+)""",
    """({event_code}4745)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^"']+)""",
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>({group_name}[^<]+)""",
    """<Data Name\\*=('|")TargetDomainName('|")>({group_domain}[^<]+)<""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>"""
    """<Data Name\\*=('|")TargetSid('|")>({group_id}[^<]+)""",
    """<Data Name\\*=('|")PrivilegeList('|")>({privileges}[^<]+?)<""",
    """<Level>({run_level}[^<]+)<"""
    ]


}
```