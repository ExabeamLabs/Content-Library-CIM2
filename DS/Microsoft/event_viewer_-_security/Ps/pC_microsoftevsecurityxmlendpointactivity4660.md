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
    """<Data Name(\\)?=('|")SubjectIP('|").*?>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}.+?)</Data>""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>({domain}.+?)</Data>""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>({user}.+?)</Data>""",
    """<Data Name(\\)?=('|")ObjectServer('|")>({object_server}.+?)</Data>""",
    """<Data Name(\\)?=('|")ObjectType('|")>({object_class}.+?)</Data>""",
    """<Data Name(\\)?=('|")ObjectName('|")>({object}.+?)</Data>""",
    """<Data Name(\\)?=('|")(HandleID|HandleId)('|")>({object_id}.+?)</Data>""",
    """<Data Name =('|")ProcessName('|")>\s*({process_path}({process_dir}[^"<]+?)({process_name}[^"<\\]+))\s*</Data>""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)""",
    """<EventName>({event_name}[^<]+)<\/EventName>"""
]


}
```