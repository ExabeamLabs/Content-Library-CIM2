#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4764
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4764</EventID>""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing""" , """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """Guid\\*=('|")\{({process_guid}[^\"\\'}]+)""",
    """({event_code}4764)""",
    """ThreadID(\\)?=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """Provider Name\\*=('|")({provider_name}[^\"]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^"]+)""",
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>({group_name}[^<]+)""",
    """<Data Name\\*=('|")TargetDomainName('|")>({group_domain}[^<]+)<""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>"""
    """<Data Name\\*=('|")TargetSid">({group_id}[^<]+)""",
    """<Data Name\\*=('|")PrivilegeList('|")>({privileges}[^<]+?)<""",  
    """<Data Name =('|")GroupTypeChange('|")>({additional_info}[^<]+)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```