#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-authentication-fail-5723
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """5723""", """The session setup from computer""", """failed because the security database does not contain""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}5723)""",
        """({event_name}The session setup from computer.+?)\.""",
        """trust account\s*'({user}[^']+)""",
  ]


}
```