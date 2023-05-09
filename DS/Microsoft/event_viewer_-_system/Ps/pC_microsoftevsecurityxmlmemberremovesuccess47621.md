#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-member-remove-success-4762-1
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""<EventID>4762</EventID>""", """<Data Name""" ,"""Distribution Group Management""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """Provider Name\\*='({provider_name}[^\']+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
    """<Data Name\\*='MemberSid'>({account_id}[^<]+)<""",
    """<Data Name\\*='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name\\*='TargetUserName'>({group_name}[^<]+)""",
    """<Data Name\\*='TargetDomainName'>({group_domain}[^<]+)<""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[^<]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)"""
  ]


}
```