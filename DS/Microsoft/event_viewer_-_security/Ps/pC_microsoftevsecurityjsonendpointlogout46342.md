#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-4634-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"EventID":"4634"""", """An account was logged off""" ]
  Fields = [
    """({event_name}An account was logged off)""",
    """({event_code}4634)""",
    """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[^"]+)"""",
    """"Keywords":"({result}[^"]+)""",
    """"TargetUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"TargetLogonId":"({login_id}[^"]+)"""",
    """"TargetDomainName":"({domain}[^"]+)"""",
    """"TargetUserSid":"({user_sid}[^"]+)"""",
  ]
  DupFields = ["host->dest_host"]


}
```