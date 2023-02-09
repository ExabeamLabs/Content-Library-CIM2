#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-authentication-4774
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4774""", """An account was mapped for logon""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}4774)""",
        """({event_name}An account was mapped for logon)""",
        """Account UPN:\s*(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[^\s\\\/]+)""",
        """Mapped Name:\s*({account}[^\s]+)""",
        """Authentication Package:\s*({auth_package}[^\s]+)""",
  ]


}
```