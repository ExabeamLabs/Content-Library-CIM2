#### Parser Content
```Java
{
Name = microsoft-evpowershell-kv-process-create-success-executing
  Vendor = Microsoft
  Product = Event Viewer - PowerShell 
  ParserVersion = v1.0.0
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "EEE MMM dd HH:mm:ss yyyy"]
  Conditions = [
"""Microsoft-Windows-PowerShell""",
"""Context:"""
  ]
  Fields = [
    """\$Message\s*=\s*"({event_name}[^"]+)""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s""",
    """({time}\w{3}\s\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({dest_host}({host}[\w.\-]+))""",
    """<EventID[^>]*>({event_code}\d+)<\/EventID>""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """Sid=({user_sid}[\w\-]+)""",
    """<Execution ProcessID\\*='({process_id}\d+)""",
    """<Security UserID\\*='({user_sid}[\w\-]+)'/>""",
    """Context[^\]]+?User\s*\\?=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""",
    """Context[^@]+?Host Application\s*=\s*({process_command_line}.+?)\s*Engine Version =""",
    """Context[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+)[^\n]+?)\s+Engine Version =""",
    """Context[^@]+?Command Type\s*=\s*(|({command_type}[^=]+?))\s*Script Name =""",
    """Context[^@]+?Command Name\s*=\s*(|({command}[^=]+?))\s*Command Type =""",
    """Context[^@]+?Script Name\s*=\s+({script_name}\S[^=]+?)\s+Command Path =""",
    """CommandInvocation(.+?):\s*\\*"({command_invocation}[^"\\]+)\\?"""",
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