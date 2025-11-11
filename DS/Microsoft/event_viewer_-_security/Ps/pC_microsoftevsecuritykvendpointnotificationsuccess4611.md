#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4611
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""EventCode=4611""", """A trusted logon process has been registered"""]
  Fields = [
    """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
    """ComputerName =({dest_host}({host}[\w.\-]+))""",
    """EventCode=({event_code}\d+)""",
    """Security ID:\s+({user_sid}.+?)\s+Account Name:\s+(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+(?=\w)({domain}.+?)\s+Logon ID""",
    """Logon ID:\s+({login_id}.+?)\s+Logon Process Name:\s+({process_name}[^\s]+)"""
  ]


}
```