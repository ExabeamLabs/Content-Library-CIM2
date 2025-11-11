#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4627
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4627</EventID>""", """Name ='GroupMembership'""", """TargetUserName""" ]
  Fields = [
    """({event_name}GroupMembership)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({dest_user_sid}({user_sid}[^<]+))<""",
    """<Data Name\\*=('|")TargetUserSid('|")>({dest_user_sid}({user_sid}[^<]+))<""",
    """<Data Name\\*=('|")TargetLogonId('|")>({dest_login_id}({login_id}[^<]+))<""",
    """<Data Name\\*=('|")TargetUserName('|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name\\*=('|")LogonType('|")>({login_type}\d+)<""",
    """ProcessID\\*=('|")({process_id}\d+)('|")""",
    """ThreadID\\*=('|")({thread_id}\d+)('|")""",
    """<Keywords>({action}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)""",
    """<Data Name\\*=('|")TargetDomainName('|")>({dest_domain}({domain}[^<]+))<""",
    """<Level>({run_level}[^<]+)<"""
# user_groups is removed
  ]


}
```