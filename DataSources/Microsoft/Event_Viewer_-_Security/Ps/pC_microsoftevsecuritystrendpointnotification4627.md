#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-notification-4627
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4627""", """Group membership information""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)""",
    """EVENT_ID="({event_code}\d+)"""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|({host}[^\s]+))""",
    """({event_name}Group membership information)""",
    """Subject:[^"]+?Security ID:\s*((NT AUTHORITY|([^\\:]+))\\+)?(SYSTEM|\\NULL SID|({user_sid}[^:\s]+))""",
    """Subject:[^"]+?Account Name:\s*(-|({account_name}[^\s]+))""",
    """Subject:[^"]+?Account Domain:\s*(-|({account_domain}[^\s]+))""",
    """Subject:[^"]+?Logon ID:\s*({login_id}[^\s]+)""",
    """New Logon:[^"]+?Security ID:\s*((NT AUTHORITY|([^\\:]+))\\+)?(SYSTEM|ANONYMOUS|({user_sid}[^:\s]+))\s[^:]*?Account Name:""",
    """New Logon:[^"]+?Account Name:\s*(SYSTEM|ANONYMOUS|({user}[^\s]+))""",
    """New Logon:[^"]+?Account Domain:\s*(NT AUTHORITY|({domain}[^\s]+))""",
    """New Logon:[^"]+?Logon ID:\s*({login_id}[^\s]+)""",
# DL Fields are removed
    """Logon Type:\s*({login_type}\d+)""",
    """sourceip="({src_ip}[a-fA-F\d:.]+)"""",
    """EVENT_TYPE="({result}[^"]+)""""
  ]


}
```