#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-read-5379"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """5379""", """Credential Manager credentials were read""", """(EventID 5379)""", """Microsoft Windows security auditing""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+MSWinEventLog""",  
    """Logon ID:\s*({login_id}[^\s]+)\s+Read Operation:""",
    """Security ID:\s*(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({user_sid}[^:]+?))\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|({user}[^\s]+))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}[^\s]+))\s+Logon ID:""",
    """({event_name}Credential Manager credentials were read)"""
 ]


}
```