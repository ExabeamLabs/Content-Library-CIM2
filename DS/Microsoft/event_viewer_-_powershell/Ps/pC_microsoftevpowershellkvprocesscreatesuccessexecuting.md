#### Parser Content
```Java
{
Name = microsoft-evpowershell-kv-process-create-success-executing
  Vendor = Microsoft
  Product = Event Viewer - PowerShell 
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
"""Microsoft-Windows-PowerShell""",
"""Context:"""
  ]
  Fields = [
    """\$Message\s*=\s*"({event_name}[^"]+)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
    """<TimeCreated SystemTime\\*='({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d{3})""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({dest_host}({host}[\w.\-]+))""",
    """<EventID[^>]*>({event_code}\d+)<\/EventID>""",
    """<Computer>({dest_host}({host}[^<>]+))</Computer>""",
    """Sid=({user_sid}[\w\-]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Security UserID\\*='({user_sid}[\w\-]+)'/>""",
    """Context[^@]+?User\s*=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[^=\/\\]+?))\s*Connected User =""",
    """Context[^@]+?Host Application\s*=\s*({process_command_line}.+?)\s*Engine Version =""",
    """Context[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+)[^\n]+?)\s+Engine Version =""",
    """Context[^@]+?Command Type\s*=\s*(|({command_type}[^=]+?))\s*Script Name =""",
    """Context[^@]+?Command Name\s*=\s*(|({command_name}[^=]+?))\s*Command Type =""",
    """Context[^@]+?Script Name\s*=\s+({script_name}\S[^=]+?)\s+Command Path =""",
    """Engine Version\s*=\s*({engine_version}[^\s]+)\s*"""
    """"(?:winlog\.)?computer_name"\s*:\s*"({dest_host}({host}[\w\-\.]+))"""
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """"domain":"({domain}[^"]+)""""
    """"event_id":({event_code}\d+)"""
    """"user"\s*:\s*\{[^\}]*"identifier"\s*:\s*"({user_sid}[^"]+)"""
    """"process_id":({process_id}\d+)"""
]


}
```