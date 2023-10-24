#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-authentication-4774-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """EVENT_ID="4774"""", """EVENT_TASK="Credential Validation"""", """An account was mapped for logon""" ]
  Fields = [
    """({event_name}An account was mapped for logon)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+)\s({host}[^\s]+)""",
    """sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """EVENT_ID="*({event_code}\d+)""",
    """Account UPN:\s*(?:({user_type}host)\/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """Mapped Name:\s*({account}[^\s\<]+)""",
  ]


}
```