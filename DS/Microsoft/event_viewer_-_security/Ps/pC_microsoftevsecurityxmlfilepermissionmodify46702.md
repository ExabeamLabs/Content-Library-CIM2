#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-permission-modify-4670-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4670</EventID>""", """<Data Name""","""SubjectUserName""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name\\*=('|")ObjectServer('|")>(-|({object_server}[^<]+))</Data>""",
    """<Data Name\\*=('|")ObjectType('|")>(-|({object_type}[^<]+))</Data>""",
    """<Data Name\\*=('|")ObjectName('|")>(-|({object_name}[^<]+))</Data>""",
    """<Data Name\\*=('|")ProcessId('|")>(-|({process_id}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>(-|({user_sid}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectUserName('|")>(-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name\\*=('|")SubjectDomainName('|")>(-|({domain}[^<]+))</Data>""",
    """<Data Name\\*=('|")SubjectLogonId('|")>(-|({login_id}[^<]+))</Data>""",
    """<Data Name\\*=('|")ProcessName('|")>(-|({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?(\.({file_ext}[^\\\/\.<]+)))))</Data>"""
    """Permissions Change:[\s\S]*?((\\)*(\\r|\\t|\\n))*\s*({attribute}[^<=]+?)\s*(\w+=|<)""",
    """Permissions Change:[\s\S]*?New Security Descriptor:[^\S<]*({permissions}[^<]+?)(\s+|<)""",
    """({event_name}Permissions on an object were changed)""",
    """<Data Name\\*=('|")OldSd('|")>({old_attribute}[^<]+)<""",
    """<Data Name\\*=('|")NewSd('|")>({new_attribute}[^<]+)<""",
    """<Data Name\\*=('|")HandleId('|")>({object_id}[^<]+)<""",
    """<Keywords>({result}[^<>]+)</Keywords>""",
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = ["process_name -> file_name", "process_path -> file_path", "process_dir -> file_dir", "user->src_user", "domain->src_domain"]


}
```