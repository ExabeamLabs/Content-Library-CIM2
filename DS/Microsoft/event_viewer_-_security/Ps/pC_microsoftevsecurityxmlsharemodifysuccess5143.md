#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-share-modify-success-5143
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>5143""", """<Data Name""","""SubjectUserSid"""]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({host}[\w\-.]{1,20000})<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}5143)""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<""",
    """<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
     """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<""",
    """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<""",
    """<Data Name\\*=('|")ObjectType('|")>({file_type}[^<]+)<""",
    """<Data Name\\*=('|")ShareName('|")>(?:[\\\*]+)?({share_name}[^<]+)<""",
     """<Data Name\\*=('|")ShareLocalPath('|")>[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))<""",
    """<Message>({event_name}A network share object was modified)""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]


}
```