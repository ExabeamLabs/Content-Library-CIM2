#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-create-success-4731
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS"
  Conditions = [ """A security-enabled local group was created""", """<EventID>4731</EventID>""" ]
  Fields = [
    """({event_name}A security-enabled local group was created)""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime\\?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9})""",
    """({event_code}4731)""",
    """<Data Name\\?='SubjectUserSid'>(-|({user_sid}[^<>]+))<""",
    """<Data Name\\?='SubjectUserName'>(-|({user}[\w\.\-]{1,40}\$?))<""",
    """<Data Name\\?='SubjectDomainName'>(-|({domain}[^<>]+))<""",
    """<Data Name\\?='SubjectLogonId'>(-|({login_id}[^<>]+))<""",
    """<Data Name\\?='TargetUserName'>({group_name}[^<]+)<""",
    """<Data Name\\?='TargetDomainName'>({group_domain}[^<]+)<""",
    """<Data Name\\?='TargetSid'>({group_id}[^<]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```