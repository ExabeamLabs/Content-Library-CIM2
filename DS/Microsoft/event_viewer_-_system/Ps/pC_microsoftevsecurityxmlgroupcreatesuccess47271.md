#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-create-success-4727-1
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4727</EventID>""" ,"""Security Group Management""" ,"""<Execution ProcessID""" ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Data Name\\*='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)</Data>"""	
] 


}
```