#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-handle-request-4656
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [ """<EventID>4656</EventID>""", """SubjectUserSid""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{7,9}Z)"""
    """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}[^<>]+)<""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(NT AUTHORITY|({domain}[^<>]+))<""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name(\\)?=('|")ObjectServer('|")>({object_server}[^<>]+)<""",
    """<Data Name(\\)?=('|")ObjectType('|")>({object_class}File)</Data><Data Name(\\)?=('|")ObjectName('|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<>\\\/]+?(\.({file_ext}[^<>\\\/\.]+?))?)))<""",
    """<Data Name(\\)?=('|")ObjectType('|")>({object_class}Process)</Data><Data Name(\\)?=('|")ObjectName('|")>(-|({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^<\\\/]+?)))<""",
    """<Data Name(\\)?=('|")ObjectType('|")>({object_class}Key)<\/Data><Data Name(\\)?=('|")ObjectName('|")>(-|({registry_path}[^<]*?({registry_key}[^<\\\/]+?)))<""",
    """<Data Name(\\)?=('|")ObjectType('|")>(?!(File|Process|Key))({object_class}[^<]+?)</Data><Data Name(\\)?=('|")ObjectName('|")>(-|({object}[^<]+?))<""",
    """<Data Name(\\)?=('|")(HandleID|HandleId)('|")>({object_id}[^<>]+)<""",
    """<Data Name(\\)?=('|")DesiredAccess('|")>\s*({access}[^<>]+)\s*<""",
    """<Data Name(\\)?=('|")ProcessName('|")>\s*({process_path}({process_dir}(?:[^<]+)?[\\\/]+)?({process_name}[^\\\/"<]+?))\s*</Data>""",
    """<Message>({event_name}[^\.]+)""",
    """<Data Name(\\)?='SubjectLogonId'>({login_id}[^<]+)""",
    """<Keywords>({result}[^<]+)<""",
    """<Level>({run_level}[^<]+)<"""
    """Transaction ID:\s*\{({transaction_id}[^\s\}]+)\}?\s*Accesses:""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """({operation_type}requested)""",
    """Handle ID:\s*({handle_id}\S+)""",
    """Accesses:\s*({access}\S.*?)\s*Access Reasons:""",
    """Access Reasons:\s*(-|({access}\S.*?))\s*Access Mask:""",
  ]
  DupFields = ["user->src_user", "domain->src_domain", "object_class->object_type"]


}
```