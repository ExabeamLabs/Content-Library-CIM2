#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-list-4798
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4798<""", """Microsoft-Windows-Security-Auditing""", """<Data Name\=""", """TargetUserName""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-3-dl.Fields}[
    """<Computer>({host}[^<>]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_name}A user's local group membership was enumerated)""",
    """<Level>({run_level}[^<]+)<"""
  ]

windows-events-3-dl = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<TimeCreated SystemTime\\='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
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
    """<Data Name\\='SubjectLogonId'>(-|({login_id}[^<>]+))<"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  
}
```