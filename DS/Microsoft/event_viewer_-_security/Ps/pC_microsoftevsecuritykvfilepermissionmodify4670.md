#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-permission-modify-4670
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy","MM/dd/yyyy hh:mm:ss a"]
  Conditions = ["""Permissions on an object were changed"""]
  Fields = [
    """({event_name}Permissions on an object were changed)""",
    """({event_code}4670)""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))""",
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+""",
    """(::ffff:)?({host}[^\s=]+)\sMSWinEventLog""",
    """Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s""",
    """Security ID:\s*(SYSTEM|({user_sid}[^\s]+))\s""",
    """Account Name:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+(\s\w+)?:""",
    """Account Domain:\s*({domain}[^\s]+)\s""",
    """Logon ID:\s*({login_id}[^\s]+)\s""",
    """Process ID:\s*({process_id}[^\s]+)\s""",
    """Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s+""",
    """Process Name:\s*(.+?[\\\/]+)?({file_name}[^\s\\\/]+?(\.({file_ext}[^\s\\.\/]+?))?)\s""",
    """Handle ID:\s*({object_id}.+?)\s""",
    """Object Type:\s*({object_type}[^\s]+)\s""",
    """Object Name:\s*(-|({object}[^\s]+))\s""",
    """Permissions Change:\s*({attribute}[^\s].+?)\s+(User:|$)""",
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
    """Permissions Change:[\s\S]*?New Security Descriptor:[^\S<]*({permissions}[^<]+?)(\s+|<)"""
  ]


}
```