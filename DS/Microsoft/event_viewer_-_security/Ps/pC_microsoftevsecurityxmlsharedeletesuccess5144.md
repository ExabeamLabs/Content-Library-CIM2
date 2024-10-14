#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-delete-success-5144"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<EventID>5144</EventID>""", """Microsoft-Windows-Security-Auditing""", """<Data Name""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}A network share object was deleted)""",
    """<Computer>({host}({dest_host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}5144)</EventID>""",
    """<Data Name\\*='ShareName'>[\\*]+({share_name}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*='ShareLocalPath'>({share_path}[^<]+)<\/Data>""",
    """<Data Name\\*='SubjectLogonId'>({login_id}[^<]+)<\/Data>""",
    """<Keyword>({result}[^<]+)<\/Keyword>""",
    """<Data Name\\*='SubjectUserName'>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```