#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-permission-modify-4670-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4670<""", """Permissions on an object were changed""", """<Data Name\=""", """ObjectServer""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-3-dl.Fields}[
    """<Computer>({host}[^<>]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({event_name}Permissions on an object were changed)""",
    """<Data Name\\=('|")HandleId('|")>({object_id}[^<]+)<""",
    """<Data Name\\=('|")ObjectServer('|")>(-|({object_server}[^<]+))<""",
    """<Data Name\\=('|")ObjectType('|")>(-|({object_type}[^<]+))<""",
    """<Data Name\\=('|")ObjectName('|")>(-|({object}[^<]+))<""",
    """<Data Name\\=('|")OldSd('|")>({old_attribute}[^<]+)<""",
    """<Data Name\\=('|")NewSd('|")>({new_attribute}[^<]+)<""",
    """<Level>({run_level}[^<]+)<""",
    """<Data Name\\=('|")(Caller)?ProcessName('|")>(-|(([^<>]*?[\\\/]+)?({file_name}[^<>\\\/]+?(\.({file_ext}[^\s\.\\\/<>]+))?)))<"""
  ]

windows-events-3-dl = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<TimeCreated SystemTime\\=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """<Keywords>({result}[^<>]+)</Keywords>""",
    """<Data Name\\=('|")(Caller)?ProcessName('|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<""",
    """<Data Name\\=('|")(Caller)?ProcessId('|")>({process_id}[^<]+?)\s*<""",
    """<Execution ProcessID\\=('|")({process_id}[^'"]+)""",
    """<EventID>({event_code}\d+)""",
    """<Data Name\\=('|")TargetUserName('|")>(SYSTEM|({dest_user}[^<]+))<""",
    """<Data Name\\=('|")TargetDomainName('|")>({dest_domain}[^<]+)<""",
    """<Data Name\\=('|")LogonType('|")>({login_type}\d+)<""",
    """<Data Name\\=('|")TargetUserSid('|")>({dest_user_sid}[^<]+)<""",
    """<Data Name\\=('|")TargetLogonId('|")>({dest_login_id}[^<]+)<"""
    """<Data Name\\=('|")SubjectUserSid('|")>(-|({user_sid}[^<>]+))<""",
    """<Data Name\\=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name\\=('|")SubjectDomainName('|")>(-|({domain}[^<>]+))<""",
    """<Data Name\\=('|")SubjectLogonId('|")>(-|({login_id}[^<>]+))<"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  ]
  DupFields = ["user->src_user", "domain->src_domain"
}
```