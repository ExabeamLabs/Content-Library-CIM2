#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-name-modify-4781-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4781<""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({event_code}4781)""",
    """<Data Name\\*=('|")OldTargetUserName">(-|({old_user_name}[^<]+))<""",
    """<Data Name\\*=('|")NewTargetUserName">(-|({new_user_name}[^<]+))<""",
    """<Data Name\\*=('|")TargetDomainName">(-|({dest_domain}[^<]+))<""",
    """<Data Name\\*=('|")TargetSid">(-|({dest_user_sid}[^<]+))<""",
    """<Data Name\\*=('|")SubjectUserSid">(-|({user_sid}[^<]+))<""",
    """<Data Name\\*=('|")SubjectUserName">(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name\\*=('|")SubjectDomainName">(-|({domain}[^<]+))<""",
    """<Data Name\\*=('|")SubjectLogonId">(-|({login_id}[^<]+))<""",
    """<Data Name\\*=('|")PrivilegeList">(-|({privileges}[^<]+))<""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "new_user_name->dest_user", "user->src_user", "domain->src_domain" ]


}
```