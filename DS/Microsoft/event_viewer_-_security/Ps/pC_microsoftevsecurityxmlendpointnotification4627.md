#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4627
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4627</EventID>""", """<Task>Group Membership""", """Group membership information""" ]
  Fields = [
    """({event_name}Group membership information)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+?)<""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+?)<""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<""",
    """<Data Name\\*=('|")SubjectUserName('|")>(-|({account_name}[^<]+))<""",
    """<Data Name\\*=('|")SubjectDomainName('|")>(-|({account_domain}[^<]+))<""",
    """<Data Name\\*=('|")SubjectLogonId('|")>(-|({login_id}[^<]+))<""",
    """<Data Name\\*=('|")TargetUserSid('|")>({user_sid}[^<]+)<""",
    """<Data Name\\*=('|")TargetUserName('|")>({user}[\w\.\-]{1,40}\$?)<""",
    """<Data Name\\*=('|")TargetDomainName('|")>({domain}[^<]+)<""",
    """<Data Name\\*=('|")TargetLogonId('|")>({login_id}[^<]+)<""",
    """<Data Name\\*=('|")LogonType('|")>({login_type}\d+)<""",
# sequence_num is removed
# user_groups is removed
  ]


}
```