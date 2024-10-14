#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-logout-4634
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [ """<EventID>4634</EventID>""", """<TimeCreated SystemTime""", """<Data Name""" ]
  Fields = [
    """<Message>({event_name}[^.。]+)""",
    """({event_name}An account was logged off)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")\/>""",
    """<Computer>([^<>]+?[\\\/]+)?({src_host}({host}[\w\-.]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Data Name\\*=('|")LogonType('|")>({login_type}\d+)<\/Data>""",
    """<Data Name\\*=('|")TargetUserSid('|")>({user_sid}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")TargetDomainName('|")>((?i)NT AUTHORITY|({domain}[^<]+))<\/Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>((?i)SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>""",
    """<Data Name\\*=('|")TargetLogonId('|")>({login_id}[^<]+)<\/Data>"""
    """<Data Name\\*=('|")(Caller)?ProcessId('|")>({process_id}[^<]+?)\s*<""",
    """<Execution ProcessID\\*=('|")({process_id}[^'"]+)""",
    """Logon Type\s*:\s*(-|({login_type}\d+))\s+"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "user->dest_user","user_sid->dest_user_sid","domain->dest_domain","login_id->dest_login_id"]


}
```