#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-process-create-success-800-1
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<Provider Name"""
"""'PowerShell""",
""">800</EventID>""",
"""<Computer>"""
  ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """UserId\\*=({domain}[^\\]+)\\({user}[\w\.\-]{1,40}\$?)\s*HostName""",
    """({event_code}800)""",
    """ScriptName\\*=\s*(|({process_path}({process_dir}([\w:]+\\)?([^\\]+?\\)*?)({process_name}[^\\=]*?)))\s+CommandLine""",
    """HostApplication\\*=\s*({powershell_image}[^=]+?)\s+EngineVersion=""",
    """CommandLine\\*=\s*({process_command_line}[^<]+?)\s*<\/Data>""",
    """<Data>CommandInvocation[^<]{0,10000}value="+\s*(|-|({command_module}.+?))\s*"\s*<\/Data>""",
    """<Data>CommandInvocation[^:]+:\s*"+({command_invocation}[^"]+)"""
    """<Level>({run_level}[^<]+)<"""
]


}
```