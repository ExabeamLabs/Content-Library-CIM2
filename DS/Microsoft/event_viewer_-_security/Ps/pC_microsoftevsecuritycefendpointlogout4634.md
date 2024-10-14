#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-logout-4634
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4634<""", """An account was logged off""", """<Data Name\=""", """TargetUserName""" ]
  Fields = [
    """<TimeCreated SystemTime\\='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """<Computer>({src_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Keywords>({result}[^<>]+)</Keywords>""",
    """<Data Name\\='(Caller)?ProcessName'>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<""",
    """<Data Name\\='(Caller)?ProcessId'>({process_id}[^<]+?)\s*<""",
    """<Execution ProcessID\\='({process_id}[^'"]+)""",
    """<EventID>({event_code}\d+)""",
    """<Data Name\\='TargetUserName'>(SYSTEM|({dest_user}[^<]+))<""",
    """<Data Name\\='TargetDomainName'>({dest_domain}[^<]+)<""",
    """<Data Name\\='LogonType'>({login_type}\d+)<""",
    """<Data Name\\='TargetUserSid'>({dest_user_sid}[^<]+)<""",
    """<Data Name\\='TargetLogonId'>({dest_login_id}[^<]+)<"""
    """<Data Name\\='SubjectUserSid'>(-|({user_sid}[^<>]+))<""",
    """<Data Name\\='SubjectUserName'>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name\\='SubjectDomainName'>(-|({domain}[^<>]+))<""",
    """<Data Name\\='SubjectLogonId'>(-|({login_id}[^<>]+))<""",
    """({event_name}An account was logged off)"""
  ]
  DupFields = [ "dest_user->user", "dest_user_sid->user_sid", "dest_login_id->login_id", "dest_domain->domain" ]


}
```