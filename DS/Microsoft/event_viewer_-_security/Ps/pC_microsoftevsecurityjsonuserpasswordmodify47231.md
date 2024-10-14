#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-password-modify-4723-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"EventID":4723"""
  """"SourceModuleType":"""
]
Fields = [
  """({event_name}An attempt was made to change an account's password)"""
  """"EventTime":\s*"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""""
  """"Hostname":"({host}[\w\-.]*)"""
  """"SubjectUserSid":"({user_sid}[^"]+)"""
  """"EventType":"({result}[^"]+)"""
  """({event_code}4723)"""
  """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"SubjectDomainName":"({domain}[^"]+)"""
  """"SubjectLogonId":"({login_id}[^"]+)"""
  """"TargetSid":"({dest_user_sid}[^"]+)"""
  """"TargetUserName":"({dest_user}[^"]+)"""
  """"TargetDomainName":"({dest_domain}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```