#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-modify-success-4738-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"SubjectUserName":"""", """"A user account was changed""", """"OperationName":"MICROSOFT.AAD/DomainServices/Events/Security/4738"""" ]
  Fields = [
    """({event_name}A user account was changed)""",
    """({event_code}4738)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"Category"+:"+({category}[^"]+)"""",
    """"TargetSid":"({target_sid}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```