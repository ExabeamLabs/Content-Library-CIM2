#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-4611
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss"]
  Conditions = [ """A trusted logon process has been registered""", """(EventID 4611)""", """Microsoft Windows security auditing"""]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({event_name}A trusted logon process has been registered)""",
    """\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(\d{4}|({host}[\w\-.]+))\s\w+""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)"""
    """({event_code}4611)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+MSWinEventLog""",
    """Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+(?=\w)({domain}[^:]+?)\s+Logon ID""",
    """Logon ID:\s+({login_id}[^\s]+)\s+Logon Process Name:\s+({process_name}[^\s]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```