#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-handle-close-4658
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """4658""", """<Data Name""", """The handle to an object was closed""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_code}4658)""",
    """({event_name}The handle to an object was closed)""",
    """"Activity":"({event_name}[^"]+)""",
    """(<|")Computer(>|"):?"?({host}[^"<]+)""",
    """<Data Name\\*='SubjectUserSid'>({user_sid}[^<>]+)</Data>""",
    """<Data Name\\*='SubjectUserName'>(SYSTEM|({user}[\w\.\-]{1,40}\$?))</Data>""",
    """<Data Name\\*='SubjectDomainName'>(NT AUTHORITY|({domain}[^<>]+))</Data>""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name\\*='ObjectServer'>({object_server}[^<>]+)</Data>""",
    """<Data Name\\*='ProcessId'>({process_id}[^<>]+)</Data>""",
    """<Data Name\\*='ProcessName'>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>""",
    """({operation_type}closed)""",
    """<Data Name\\*='HandleId'>({object_id}[^<>]+)</Data>"""
  ]


}
```