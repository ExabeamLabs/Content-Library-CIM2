#### Parser Content
```Java
{
Name = microsoft-windows-mix-configuration-modify-success-4739
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """Domain Policy was changed""", """<EventID>4739<""", """='SubjectUserName'>""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}({dest_host}[^<>]+))<""",
    """({event_name}Domain Policy was changed)""",
    """<Execution ProcessID(\\)?='({process_id}[^']+)""",
    """<EventID>({event_code}\d+)</EventID>""",
    """<Keyword>({action}[^<]+)<""",
    """<Data Name\\?='SubjectUserSid'>({user_sid}[^<]+)<\/Data>""",
    """ThreadID\\?='({thread_id}\d+)""",
    """<Data Name\\?='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """<Data Name\\?='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\?='SubjectLogonId'>({login_id}[^<]+)<\/Data>"""
  ]
  ParserVersion = "v1.0.0"


}
```