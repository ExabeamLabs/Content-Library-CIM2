#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-log-clear-success-logfileclear
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [""">1102</EventID>""",  """<Channel>Security</Channel>""", """<LogFileCleared""" ]
  Fields = [
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)""",
    """<Computer>({host}[\w\-.]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Computer>(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))"""
    """<SubjectLogonId>({login_id}[^<]+)""",
    """({event_code}1102)""",
    """({event_name}LogFileCleared)""",
    """<SubjectUserName>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """<SubjectUserSid>({user_sid}[^<]+)""",
    """<SubjectDomainName>({src_domain}({domain}[^<]+))""",
    """log_name:\s*({log_name}\s*[^,]+)""",
    """<Execution ProcessID\\*=('|")({process_id}[^"']+)""",
    """ThreadID\\*=('|")({thread_id}\d+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}[^"']+)"""
    """<Security UserID=('|")({user_sid}S-[^<]+)('|")"""
  ]
  ParserVersion = "v1.0.0"


}
```