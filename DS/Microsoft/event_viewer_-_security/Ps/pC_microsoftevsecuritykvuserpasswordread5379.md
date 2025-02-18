#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-password-read-5379"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a"]
  Conditions = [ """5379""", """Credential Manager credentials were read""", """Account Name:""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s*\d\d:\d\d:\d\d\s*((?i)AM|PM))\s*.*?LogName =""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+MSWinEventLog""",
    """"(?i)Computer(Name)?":\s*"({host}[^"]+)"""",
    """ComputerName =({host}[^\s]+)\sSourceName =""",
    """EventCode=({event_code}\d+)\s*EventType=""",
    """Logon ID:\s*({login_id}[^\s]+)\s+Read Operation:""",
    """Security ID:\s*(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({user_sid}[^:]+?))\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}[^\s]+))\s+Logon ID:""",
    """({event_name}Credential Manager credentials were read)"""
 ]


}
```