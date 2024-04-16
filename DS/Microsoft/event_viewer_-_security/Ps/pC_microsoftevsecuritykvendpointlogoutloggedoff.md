#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-logout-loggedoff
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""An account was logged off""","""Logon ID:""" ]
  Fields = [
    """({event_name}An account was logged off)""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(Administrator|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}[^:\s]+?))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Logon Type:""",
    """Logon Type:\s*({login_type}\d+)?\s*({additional_info}[^=]+?)\s*("|$)""",
  ]


}
```