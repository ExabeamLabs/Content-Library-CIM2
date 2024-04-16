#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-ds-replication-modify-4931
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4931""", """An Active Directory replica destination naming context was modified""" ]
  Fields = [
        """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
        """:\d+\s({host}[^\s]+)\sMSWinEventLog""",
        """({event_code}4931)""",
        """({event_name}An Active Directory replica destination naming context was modified)""",
        """Destination DRA:\s*({dest_host}[\w\-.]+)""",
  ]


}
```