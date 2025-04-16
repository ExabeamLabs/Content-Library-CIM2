#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4611
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4611<""" ]
  Fields = [
    """({event_name}A trusted logon process has been registered)"""
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[\w\-.]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_code}4611)""",
    """<EventRecordID>({event_id}[^<]+)""",
    """'LogonProcessName'>({auth_process}[^<"]+)<""",
    """'SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """'SubjectUserSid'>({user_sid}[^"\s<]+)<""",
    """'SubjectDomainName'>({domain}[^"\s<]+)<""",
    """'SubjectLogonId'>({login_id}[^"\s<]+)<"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```