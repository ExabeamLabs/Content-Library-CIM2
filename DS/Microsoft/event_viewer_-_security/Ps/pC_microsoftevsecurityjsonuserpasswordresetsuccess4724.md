#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-password-reset-success-4724"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"EventID":4724"""
  """"SourceModuleType"""
]
Fields = [
  """({event_name}An attempt was made to reset an account's password)"""
  """"EventTime\\?":\s*\\?"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\\?""""
  """"Hostname\\?":\\?"({host}[\w\-.]*)"""
  """({event_code}4724)"""
  """"SubjectUserSid\\?":\\?"({user_sid}[^\\"]+)"""
  """"SubjectUserName\\?":\\?"({user}[\w\.\-]{1,40}\$?)"""
  """"SubjectDomainName\\?":\\?"({domain}[^\\"]+)"""
  """"SubjectLogonId\\?":\\?"({login_id}[^\\"]+)"""
  """"TargetSid\\?":\\?"({dest_user_sid}[^\\"]+)"""
  """"TargetUserName\\?":\\?"({dest_user}[^\\"]+)"""
  """"TargetDomainName\\?":\\?"({dest_domain}[^\\"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```