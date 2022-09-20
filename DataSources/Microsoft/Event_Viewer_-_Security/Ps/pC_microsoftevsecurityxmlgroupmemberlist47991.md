#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-member-list-4799-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4799<""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}A security-enabled local group membership was enumerated)""",
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<Data Name(\\)?='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name(\\)?='SubjectUserName'>({user}[^<]+)""",
    """<Data Name(\\)?='SubjectDomainName'>({domain}[^<]+)""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)""",
    """<Data Name(\\)?='TargetSid'>({group_id}[^<]+)""",
    """<Data Name(\\)?='TargetUserName'>({group_name}[^<]+)""",
    """<Data Name(\\)?='TargetDomainName'>({group_domain}[^<]+)""",
    """<Data Name(\\)?='CallerProcessId'>({process_id}[^<]+)""",
    """<Data Name(\\)?='CallerProcessName'>({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^<\\\/]+))<\/Data>""",
  ]


}
```