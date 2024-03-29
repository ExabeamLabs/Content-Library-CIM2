#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-handle-request-4656
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4656</EventID>""", """SubjectUserSid""" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}[^<>]+)<""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(NT AUTHORITY|({domain}[^<>]+))<""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(SYSTEM|({user}[^<>]+))<""",
    """<Data Name(\\)?=('|")ObjectServer('|")>({object_server}[^<>]+)<""",
    """<Data Name(\\)?=('|")ObjectType('|")>({object_class}[^<>]+)<""",
    """<Data Name(\\)?=('|")ObjectName('|")>({object}[^<>]+)<""",
    """<Data Name(\\)?=('|")(HandleID|HandleId)('|")>({object_id}[^<>]+)<""",
    """<Data Name(\\)?=('|")DesiredAccess('|")>\s*({access}[^<>]+)\s*<""",
    """<Data Name(\\)?=('|")ProcessName('|")>\s*({process_path}({process_dir}(?:[^<]+)?[\\\/]+)?({process_name}[^\\\/"<]+?))\s*</Data>""",
    """<Message>({event_name}[^\.]+)""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)""",
    """<Keywords>({result}[^<]+)<"""
  ]


}
```