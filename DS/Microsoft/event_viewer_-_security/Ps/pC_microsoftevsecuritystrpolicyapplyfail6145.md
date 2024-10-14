#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-policy-apply-fail-6145
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """6145""", """One or more errors occured while processing security policy in the group policy objects""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}6145)""",
        """({event_name}One or more errors occured while processing security policy in the group policy objects)""",
        """Error Code:\s*({error_code}\d+)""",
        """Mapped Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]


}
```