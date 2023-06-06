#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-4627
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4627</EventID>""", """GroupMembership""", """TargetUserName""", """<Data Name""" ]
  Fields = [
    """({event_name}GroupMembership)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)<""",
    """<Data Name\\*=('|")TargetUserSid('|")>({user_sid}[^<]+)<""",
    """<Data Name\\*=('|")TargetLogonId('|")>({login_id}[^<]+)<""",
    """<Data Name\\*=('|")TargetUserName('|")>({user}[^<]+)<""",
    """<Data Name\\*=('|")LogonType('|")>({login_type}\d+)<""",
    """ProcessID\\*=('|")({process_id}\d+)('|")""",
    """ThreadID\\*=('|")({thread_id}\d+)('|")""",
    """<Keywords>({action}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)""",
    """<Data Name\\*=('|")TargetDomainName('|")>({domain}[^<]+)<""",
# user_groups is removed
  ]


}
```