#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4611
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4611<""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?='({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """<Computer>({host}[\w\-.]+)""",
    """({event_code}4611)""",
    """<EventRecordID>({event_id}[^<]+)""",
    """'LogonProcessName'>({auth_process}[^<"]+)<""",
    """'SubjectUserName'>({user}[^"\s<]+)<""",
    """'SubjectUserSid'>({user_sid}[^"\s<]+)<""",
    """'SubjectDomainName'>({domain}[^"\s<]+)<""",
    """'SubjectLogonId'>({login_id}[^"\s<]+)<"""
  ]


}
```