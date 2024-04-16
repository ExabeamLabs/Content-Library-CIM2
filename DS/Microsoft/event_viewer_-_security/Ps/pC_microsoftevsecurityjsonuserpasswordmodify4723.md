#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-password-modify-4723"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"TargetAccount":""""
  """"EventID":"4723""""
  """An attempt was made to change"""
]
Fields = [
  """({event_name}An attempt was made to change an account's password)"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"Computer":"({host}[\w\-.]+)"""
  """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""
  """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"TargetSid":"({dest_user_sid}[^\s"]+)"""
]
ParserVersion = "v1.0.0"


}
```