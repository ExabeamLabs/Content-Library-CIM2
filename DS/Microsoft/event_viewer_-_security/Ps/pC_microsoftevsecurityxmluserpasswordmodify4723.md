#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-password-modify-4723"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
  """<EventID>4723</EventID>"""
  """<Data Name"""
  """PrivilegeList"""
]
Fields = [
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
  """<Computer>({host}[\w\-.]+)</Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}[^<]+)</EventID>"""
  """<Keywords>({result}[^<]+)</Keywords>"""
  """<Keyword>({result}Audit\s[^<]+)</Keyword>"""
  """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)</Data>"""
  """<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>"""
  """<Data Name\\*=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))</Data>"""
  """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetSid('|")>({dest_user_sid}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetUserName('|")>({dest_user}[^<]+)</Data>"""
  """<Data Name\\*=('|")TargetDomainName('|")>({dest_domain}[^<]+)</Data>"""
  """({event_name}An attempt was made to change an account's password)"""
  """<Opcode>(0|({opcode}[^<]+))<"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```