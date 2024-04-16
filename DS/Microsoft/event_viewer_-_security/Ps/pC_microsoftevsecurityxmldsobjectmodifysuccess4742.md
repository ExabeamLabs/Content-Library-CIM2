#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-ds-object-modify-success-4742"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<EventID>4742</EventID>""","""<Data Name""","""TargetSid""","""TargetUserName""","""<Message>A computer account was changed"""
]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """<Message>({event_name}A computer account was changed)"""
  """<Computer>({dest_host}({host}[\w\-.]+))<"""
   """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}4742)<"""
  """<Data Name\\*=('|")TargetUserName('|")>({dest_user}[^<]+)<"""
  """<Data Name\\*=('|")TargetDomainName('|")>({ds_object_dn}[^<]+)<"""
  """<Data Name\\*=('|")SubjectUserName('|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({user}[\w\.\-]{1,40}\$?))<"""
  """<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<"""
  """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
  """<Data Name\\*=('|")UserPrincipalName('|")>(-|({attribute}[^<]+))<"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```