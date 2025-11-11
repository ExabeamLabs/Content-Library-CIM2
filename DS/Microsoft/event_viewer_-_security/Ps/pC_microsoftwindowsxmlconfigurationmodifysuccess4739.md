#### Parser Content
```Java
{
Name = microsoft-windows-xml-configuration-modify-success-4739
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [  """<EventID>4739<""", """SubjectUserName""" , """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}({dest_host}[\w\-.]+))<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_name}Domain Policy was changed)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"<>]+)""",
    """<EventID>({event_code}\d+)</EventID>""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name\\?=('|")SubjectUserSid('|")>({user_sid}[^<]+)<\/Data>""",
    """ThreadID\\?=('|")({thread_id}\d+)""",
    """<Data Name\\?=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>""",
    """<Data Name\\?=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))<\/Data>""",
    """<Data Name\\?=('|")SubjectLogonId('|")>({login_id}[^<]+)<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```