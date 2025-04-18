#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-password-reset-success-4724"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
  """<EventID>4724</EventID>""",
  """TargetSid""",
  """<Data Name""",
  """</Data>"""
]
Fields = [
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
  """<Computer>({host}({dest_host}[\w\-.]+))</Computer>"""
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}[^<]+)</EventID>"""
  """<Data Name\\*=('|")TargetSid('|")>(?:NONE_MAPPED|({dest_user_sid}[^<]+))</Data>"""
  """<Data Name\\*=('|")TargetUserName('|")>(?=\w)({dest_user}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetDomainName('|")>(?=\w)({dest_domain}[^<]+)</Data>"""
  """<Data Name\\*=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
  """<Data Name\\*=('|")SubjectUserName('|")>(?=\w)((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>"""
  """<Data Name\\*=('|")SubjectDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
  """<Data Name\\*=('|")SubjectLogonId('|")>(?=\w)({login_id}[^<]+)</Data>"""
  """<Keyword>({result}[^<]+?)<\/Keyword>"""
  """({event_name}An attempt was made to reset an account's password)"""
  """"process_id":({process_id}\d+)"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```