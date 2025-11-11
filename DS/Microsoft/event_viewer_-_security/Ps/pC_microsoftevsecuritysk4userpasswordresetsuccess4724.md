#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-user-password-reset-success-4724
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [ """"EventID":"4724"""", """An attempt was made to reset an account's password."""", """"SubjectUserName":"""", """"TargetSid":"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
    """TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """"Computer":"({dest_host}({host}[^"]+))"""",
    """"EventID":"({event_code}\d+)"""",
    """({event_name}An attempt was made to reset an account's password)""",
    """"SubjectAccount":"(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}({src_domain}[^"]+))"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"TargetDomainName":"({dest_domain}[^"]+)"""",
    """"TargetSid":"({dest_user_sid}[^"]+)"""",
    """"TargetUserName":"({dest_user}[^"]+)""""
  ]


}
```