#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-policy-apply-4954
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4954""","""Group Policy settings for Windows Firewall were changed, and the new settings were applied"""]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}4954)""",
        """({event_name}Group Policy settings for Windows Firewall were changed, and the new settings were applied)""",
  ]


}
```