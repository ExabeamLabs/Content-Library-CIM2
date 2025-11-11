#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-modify-4717
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4717</EventID>""", """<Provider Name""","""Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<EventID>({event_code}\d+)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name\\*=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """<Data Name\\*=('|")AccessGranted('|")>({access_granted_right}[^<]+)<""",
    """<Keywords>({result}[^<]+)""",
    """<Task>({sub_category}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
    """({event_name}System security access was granted to an account)""",
    """<Data Name\\*=('|")TargetSid('|")>({dest_user_sid}[^<]+)</Data>""",
    """<Data Name\\*=('|")AccessGranted('|")>({access_type}[^<]+)</Data>"""
  ]


}
```