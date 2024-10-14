#### Parser Content
```Java
{
Name = microsoft-evsystem-str-endpoint-authentication-fail-5723
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "EEE MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """5723""", """The session setup from computer""", """failed because the security database does not contain""" ]
  Fields = [
        """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
        """({time}\w{3}\s\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+""",
        """"TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}5723)""",
        """({event_name}The session setup from computer.+?)\.""",
        """trust account\s*'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
  ]


}
```