#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4737-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """<EventID>4737</EventID>""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing""","""<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """Guid\\*=('|")\{({process_guid}[^\"'\}]+)""",
    """({event_code}4737)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^"']+)""",
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
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
    DupFields = ["user->src_user", "domain->src_domain"]


}
```