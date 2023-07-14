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
    """New Logon:[^"]+?Account Name:\s*(SYSTEM|ANONYMOUS|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))""",
    """New Logon:[^"]+?Account Domain:\s*(NT AUTHORITY|({domain}[^\s]+))""",
    """New Logon:[^"]+?Logon ID:\s*({login_id}[^\s]+)""",
# DL Fields are removed
    """Logon Type:\s*({login_type}\d+)""",
    """sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """EVENT_TYPE="({result}[^"]+)""""
    """Account Name(:|=)\s*(-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s*Account Domain"""
  ]


}
```