#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-4660
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4660</EventID>""", """SubjectUserSid""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name(\\)?=('|")SubjectIP('|").*?>({src_ip}.+?)</Data>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}.+?)</Data>""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>({domain}.+?)</Data>""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>({user}.+?)</Data>""",
    """<Data Name(\\)?=('|")ObjectServer('|")>({object_server}.+?)</Data>""",
    """<Data Name(\\)?=('|")ObjectType('|")>({object_class}.+?)</Data>""",
    """<Data Name(\\)?=('|")ObjectName('|")>({object}.+?)</Data>""",
    """<Data Name(\\)?=('|")(HandleID|HandleId)('|")>({object_id}.+?)</Data>""",
    """<Data Name =('|")ProcessName('|")>\s*({process_path}({process_dir}[^"<]+?)({process_name}[^"<\\]+))\s*</Data>""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)""",
]


}
```