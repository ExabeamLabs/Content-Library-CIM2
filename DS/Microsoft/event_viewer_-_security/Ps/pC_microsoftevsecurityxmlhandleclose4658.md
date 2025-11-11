#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-handle-close-4658
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4658<""", """<Data Name""", """HandleId""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)""",
    """({event_code}4658)""",
    """<Computer>({host}[\w\-\.]+)<""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<>]+)</Data>""",
    """<Data Name\\*=('|")SubjectUserName('|")>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>(NT AUTHORITY|({src_domain}({domain}[^<>]+)))</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name\\*=('|")ObjectServer('|")>({object_server}[^<>]+)</Data>""",
    """<Data Name\\*=('|")ProcessId('|")>({process_id}[^<>]+)</Data>""",
    """<Data Name\\*=('|")ProcessName('|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>""",
    """<Data Name\\*=('|")HandleId('|")>({object_id}[^<>]+)</Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```