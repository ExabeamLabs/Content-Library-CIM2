#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-logout-4634
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """4634""", """An account was logged off""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d ((?i)am|pm))""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?((?i)am|pm|({host}[\w.\-]+))""",
    """\w+ \d+ \d\d:\d\d:\d\d (::ffff:)?((?i)am|pm|({host}[\w\-.]+))""",
    """TimeGenerated=({time}\d+)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """({event_code}4634)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\w+\s\d+\s\d+:\d+:\d+\s\d+)"""
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?((?i)am|pm|({host}[\w\-.]+))"""
    """({event_name}An account was logged off)""",
    """Security ID:\s*(SYSTEM|({user_sid}\S+))\s+Account Name:""",
    """Account Name:\s*(SYSTEM|({user}\S+))\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Logon Type:""",
    """Logon Type:\s*({login_type}\d+)""",
    """({event_code}4634)""",
    """\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|((?i)am|pm|({dest_host}[\w\-.]+)))""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?((?i)am|pm|({host}[\w\.-]+))(\s|,|"|</Computer>|$)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```