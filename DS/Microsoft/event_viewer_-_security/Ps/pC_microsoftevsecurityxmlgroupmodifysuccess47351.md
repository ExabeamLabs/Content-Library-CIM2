#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4735-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4735<""", """A security-enabled local group was changed""" , """<Channel>Security</Channel>""" ]
  Fields = [
    """<EventID>({event_code}\d+)""",
    """({event_name}A security-enabled local group was changed.)""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Execution ProcessID(\\)?='({process_id}\d+)' ThreadID(\\)?='({thread_id}\d+)'""",
    """<EventRecordID>({event_id}\d+)""",
    """<Data Name(\\)?=('|")TargetSid('|")>({group_id}[^<]+)""",
    """<Data Name(\\)?=('|")TargetUserName('|")>({group_name}[^<]+)""",
    """<Data Name(\\)?=('|")TargetDomainName('|")>({group_domain}[^<]+)""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>({domain}[^<]+)""",
    """<Data Name(\\)?=('|")SubjectLogonId('|")>({login_id}[^<]+)""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```