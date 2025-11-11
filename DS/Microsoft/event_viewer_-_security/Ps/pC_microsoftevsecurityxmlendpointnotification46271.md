#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4627-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """<EventID>4627<""" ]
  Fields = [
    """({event_name}(Group membership information|GroupMembership))""",
    """<TimeCreated SystemTime(\\)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({dest_user_sid}({user_sid}[^<]+))<""",
    """<Data Name(\\)?=('|")TargetUserSid('|")>({dest_user_sid}({user_sid}[^<]+))<""",
    """<Data Name(\\)?=('|")TargetLogonId('|")>({login_id}[^<]+)<""",
    """<Data Name(\\)?=('|")TargetUserName('|")>(({dest_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>""",
    """<Data Name(\\)?=('|")LogonType('|")>({login_type}\d+)<""",
    """ProcessID(\\)?=('|")({process_id}\d+)('|")""",
    """ThreadID(\\)?=('|")({thread_id}\d+)('|")""",
    """<Keywords>({result}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)""",
    """<Data Name(\\)?=('|")TargetDomainName('|")>({dest_domain}({domain}[^<]+))<""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```