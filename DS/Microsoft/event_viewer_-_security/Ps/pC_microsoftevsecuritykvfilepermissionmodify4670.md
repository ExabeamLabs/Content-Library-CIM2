#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-permission-modify-4670
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""Permissions on an object were changed"""]
  Fields = [
    """({event_name}Permissions on an object were changed)""",
    """({event_code}4670)""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """(::ffff:)?({host}[^\s=]+)\sMSWinEventLog""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))""",
    """Security ID:\s*(SYSTEM|({user_sid}[^\s]+))\s""",
    """Account Name:\s*(SYSTEM|({user}[\w\.\-]{1,40}\$?))\s""",
    """Account Domain:\s*({domain}[^\s]+)\s""",
    """Logon ID:\s*({login_id}[^\s]+)\s""",
    """Process ID:\s*({process_id}[^\s]+)\s""",
    """Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s+""",
    """Handle ID:\s*({object_id}.+?)\s""",
    """Object Type:\s*({object_type}[^\s]+)\s""",
    """Object Name:\s*(-|({object}[^\s]+))\s""",
    """Permissions Change:\s*({attribute}[^\s].+?)\s+(User:|$)""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]
  DupFields = ["process_name -> file_name"]


}
```