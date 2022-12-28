#### Parser Content
```Java
{
Name = microsoft-windows-kv-user-privilege-assign-success-576-1
  Vendor = Microsoft
  Product = Windows
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ "\t576\t", "Special privileges assigned to new logon:" ]
  Fields = [
    """<\d+>(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))\s""",
    """({event_name}Special privileges assigned to new logon)""",
    """\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+""",
    """({event_code}576)""",
    """Security\t([^\s]+\t){2}({result}.+?)\t""",
    """(?:Information|Audit Success|Success Audit).+?User Name:\s+(|({user}[^:]+?))\s+Domain""",
    """\s+Domain:\s+({domain}[^\s]+)""",
    """\s+Logon ID:\s+\([^,]+,({login_id}[^)]+)""",
    """\s+Privileges:\s+({privileges}.+?)\s+\d+""",
    """\s+({ownership_privilege}SeTakeOwnershipPrivilege)""",
    """\s+({environment_privilege}SeSystemEnvironmentPrivilege)""",
    """\s+({debug_privilege}SeDebugPrivilege)""",
    """\s+({tcb_privilege}SeTcbPrivilege)"""
  ]


}
```