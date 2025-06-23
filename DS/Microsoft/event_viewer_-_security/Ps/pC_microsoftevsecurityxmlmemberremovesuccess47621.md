#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-member-remove-success-4762-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""<EventID>4762</EventID>""", """<Data Name""", """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """Provider Name\\*='({provider_name}[^\']+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """<Data Name\\*='MemberSid'>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<""",
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name\\*='TargetUserName'>({group_name}[^<]+)""",
    """<Data Name\\*='TargetDomainName'>({group_domain}[^<]+)<""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Level>({run_level}[^<]+)<""",
    """<Data Name ='MemberName'>CN=({member}[^=]+?),CN=Users,"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```