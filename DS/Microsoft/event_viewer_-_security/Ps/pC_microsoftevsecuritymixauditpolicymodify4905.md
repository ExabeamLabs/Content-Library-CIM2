#### Parser Content
```Java
{
Name = microsoft-evsecurity-mix-audit-policy-modify-4905
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss", "epoch", "yyyy-MM-dd'T'HH:mm:ss.SSS"]
  Conditions = [ """An attempt was made to unregister a security event source""", """4905""" ]
  Fields = [
    """({event_name}An attempt was made to unregister a security event source)""",
    """<Computer>(::ffff:)?({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?(am|AM|pm|PM|({host}[\w.\-]+))""",
    """({event_code}4905)""",
    """\sAccount Name:\s*(|-|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Process:""",
    """\sProcess ID:\s*(|-|({process_id}.+?))\s*Process Name:\s*(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))\s*Event Source:""",
# src_id is removed
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)"""
    """\srt=({time}\d{13})"""
  ]


}
```