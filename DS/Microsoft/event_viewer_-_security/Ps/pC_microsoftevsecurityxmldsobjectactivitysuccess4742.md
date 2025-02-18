#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-ds-object-activity-success-4742
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4742<""", """コンピューター アカウントが変更されました。""" ]
  Fields = [
    """({event_name}コンピューター アカウントが変更されました。)""",
    """<Computer>({dest_host}({host}[^<]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4742)""",
    """<EventRecordID>({event_id}[^<]+)""",
    """('|")SubjectUserSid('|")>({user_sid}[^"\s<]+)<""",
    """('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """('|")SubjectDomainName('|")>({domain}[^"\s<]+)<""",
    """('|")SubjectLogonId('|")>({login_id}[^"\s<]+)<""",
    """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```