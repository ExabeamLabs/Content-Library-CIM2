#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-authentication-4774
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4774</EventID>""", """<Task>Credential Validation""", """Provider Name""" ]
  Fields = [
    """({event_name}An account was mapped for logon)""",
    """<TimeCreated SystemTime\\*='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'\/>""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """Account UPN:\s*(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """Mapped Name:\s*({account}[^\s\<]+)""",
  ]


}
```