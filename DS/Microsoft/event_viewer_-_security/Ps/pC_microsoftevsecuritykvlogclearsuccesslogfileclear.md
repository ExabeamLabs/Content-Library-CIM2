#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-log-clear-success-logfileclear
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = ["""<EventID>1102""", """LogFileCleared""" ]
  Fields = [
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)""",
    """<Computer>({host}[^<]+)""",
    """<Computer>(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))"""
    """<SubjectLogonId>({login_id}[^<]+)""",
    """({event_code}1102)""",
    """({event_name}LogFileCleared)""",
    """<SubjectUserName>({user}[^<]+)""",
    """<SubjectUserSid>({user_sid}[^<]+)""",
    """<SubjectDomainName>({domain}[^<]+)""",
    """log_name:({log_name}\s*[^,]+)""",
    """<Execution ProcessID='({process_id}[^']+)""",
    """ThreadID='({thread_id}\d+)""",
    """<Execution ProcessID(\\)?='({process_id}[^']+)"""
  ]
  ParserVersion = "v1.0.0"


}
```