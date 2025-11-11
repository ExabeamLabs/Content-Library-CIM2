#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-create-4741
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4741</EventID>""", """<Provider Name""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}\d+)""",
    """<Data Name\\*=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>({dest_user}[^<]+)""",
    """<Data Name\\*=('|")TargetDomainName('|")>({dest_domain}[^<]+)<""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)""",
    """<Keywords>({result}[^<]+)""",
    """<Level>({run_level}[^<]+)<"""
	 ]
  

}
```