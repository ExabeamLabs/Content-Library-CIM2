#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-delete-success-4726-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
  """<EventID>4726</EventID>""",
  """TargetSid""",
  """<Data Name""",
  """</Data>"""
]
Fields = [
  """({event_name}A user account was deleted)"""
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
  """<Computer>({src_host}({host}[\w\-.]+))</Computer>"""
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}[^<]+)</EventID>"""
  """<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
  """<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-]{1,40}\$?))</Data>"""
  """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>"""
  """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))</Data>"""
  """<Data Name\\*=('|")TargetUserName('|")>(?=\w)({dest_user}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({dest_domain}[^<]+)</Data>"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = [
  "dest_user->account_name"
]
ParserVersion = "v1.0.0"


}
```