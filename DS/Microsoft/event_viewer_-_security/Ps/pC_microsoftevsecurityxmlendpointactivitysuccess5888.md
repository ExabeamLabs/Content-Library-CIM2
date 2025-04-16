#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-5888
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>5888<""", """Microsoft-Windows-Security-Auditing""", """<Data Name =""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>(-|({user_sid}[^<>]+))<""",
    """<Data Name\\*=('|")SubjectUserName('|")>(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name\\*=('|")SubjectDomainName('|")>(-|({domain}[^<>]+))<""",
    """<Data Name\\*=('|")SubjectLogonId('|")>(-|({login_id}[^<>]+))<"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]
  ParserVersion = v1.0.0


}
```