#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-process-create-success-800
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""<Provider Name"""
"""'PowerShell""",
"""800</EventID>"""
  ]
  Fields = [
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z'/>""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """UserID\\*=({domain}[^\\]+)(\\?)({user}[^\s]+?)\s+HostName""",
    """Host\s*Application\s*=\s*({powershell_image}[^\s]+)\s+EngineVersion""",
    """ScriptName\\*=\s*(|({process_path}({process_dir}([\w:]+\\)?([^\\]+?\\)*?)({process_name}[^\\=]*?)))\s+CommandLine""",
    """CommandLine\\*=\s*({process_command_line}[^<]+?)\s*</Data>""",
    """Details:.+?CommandInvocation.+?ParameterBinding.+?value=\\?"(function\s)?({command_module}[^\s\,"]+)""",
    """Details:.+?CommandInvocation\(.+?\):\s*\\*\"({command_invocation}[^\"]+)""",
    """({event_code}800)"""
]


}
```