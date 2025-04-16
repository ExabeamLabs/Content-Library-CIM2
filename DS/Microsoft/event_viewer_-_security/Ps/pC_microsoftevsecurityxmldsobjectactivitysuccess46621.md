#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-ds-object-activity-success-4662-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4662<""", """オブジェクトに対して操作が実行されました。""" ]
  Fields = [
    """({event_name}オブジェクトに対して操作が実行されました。)""",
    """({event_code}4662)""",
    """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """<TimeCreated SystemTime=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")/>""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """<EventRecordID>({event_id}[^<]+)""",
    """('|")SubjectUserSid('|")>({user_sid}[^"\s<]+)<""",
    """('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """('|")SubjectDomainName('|")>({domain}[^"\s<]+)<""",
    """('|")SubjectLogonId('|")>({login_id}[^"\s<]+)<""",
    """('|")ObjectServer('|")>({object_server}[^<]+)<""",
    """('|")ObjectType('|")>\%?\{?({object_type}[^<>\{\}]+)""",
    """('|")ObjectName('|")>\%?\{?({object_name}[^<>\{\}]+)""",
    """('|")OperationType('|")>({operation}[^<]+)<""",
    """('|")HandleId('|")>({handle_id}[^<]+)<""",
    """('|")Properties('|")>[\-\\r\\n\s]*({properties}[^<]+?)[\-\\r\\n\s]*<""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"]
  ParserVersion = "v1.0.0"


}
```