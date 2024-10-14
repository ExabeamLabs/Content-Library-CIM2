#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-process-create-success-4103-1
  Vendor = Microsoft
  Product = "Event Viewer - PowerShell"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [  """>4103</EventID>""",   """CommandInvocation""", """Script Name ="""    ]
  Fields = [
    """<TimeCreated SystemTime=\'({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)\'\/>""",
    """>({event_code}4103)<""",
    """<Computer>({dest_host}[\w\.-]+)<""",
    """<Security UserID='({user_sid}[\w-]+)'""",
    """Script Name =\s+({script_name}\S[^=]+?)\s+Command Path =""",
    """User = (({domain}[^\\]+?)\\)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(Connected User|Shell ID) =""",
    """CommandInvocation\(.+?\):\s*"({command_invocation}[^"]+)""",
    """value="{0,20}(?:function\s)?({command_module}[^\s"]+)""",
    """Host\s+Application\s*=\s*({process_command_line}.+?)\s+Engine Version =""",
    """Host\s+Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version ="""
    """CommandInvocation\(.+?\):\s*\\*"({command_invocation}[^"\\]+)""",
    """Details:.+?CommandInvocation.+?ParameterBinding.+?value=\\"(function\s)?({command_module}[^\s\\,"]+)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```