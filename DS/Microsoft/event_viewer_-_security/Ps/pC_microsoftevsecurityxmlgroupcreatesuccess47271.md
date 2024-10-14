#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-create-success-4727-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4727</EventID>""" ,"""Microsoft-Windows-Security-Auditing""" ,"""<Execution ProcessID""" , """<Channel>Security</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)</Data>"""	
    """<Level>({run_level}[^<]+)<"""
] 


}
```