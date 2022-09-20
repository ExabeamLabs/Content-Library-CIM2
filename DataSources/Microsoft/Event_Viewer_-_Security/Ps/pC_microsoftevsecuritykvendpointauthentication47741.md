#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-authentication-4774-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss+SS:SS"
  Conditions = [ """EVENT_ID="4774"""", """EVENT_TASK="Credential Validation"""", """An account was mapped for logon""" ]
  Fields = [
    """({event_name}An account was mapped for logon)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)""",
    """sourceip="({src_ip}[A-Fa-f\d.:]+)"""",
    """EVENT_ID="*({event_code}\d+)""",
    """Account UPN:\s*(?:({user_type}host)\/)?(({domain}[^\\]+)\\+)?({user}[^\s\\\/]+)""",
    """Mapped Name:\s*({account}[^\s\<]+)""",
  ]


}
```