#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-modify-4717
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """<EventID>4717</EventID>""", """Authentication Policy Change""" ,"""<Execution ProcessID"""]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<Data Name\\*='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Data Name\\*='AccessGranted'>({access_granted_right}[^<]+)<""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)"""

  ]


}
```