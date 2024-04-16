#### Parser Content
```Java
{
Name = "microsoft-evpowershell-xml-process-create-success-4103"
Vendor = "Microsoft"
Product = "Event Viewer - PowerShell"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
ExtractionType = json
Conditions = [
"""Microsoft-Windows-PowerShell"""
"""Context:"""
"""<Provider Name ="""
"""<EventID>4103<"""
]
Fields = [
"""<TimeCreated SystemTime\\*=('|")({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d{3})"""
"""({event_code}4103)"""
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<Execution ProcessID\\*='({process_id}\d+)"""
"""<Security UserID\\*='({user_sid}[\w\-]+)'/>"""
"""User = (({domain}[^=]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)(\\r|\\n|\\t)*\s*(Connected User|Shell ID)\s*=""",
"""CommandInvocation(.+?):\s*"({command_invocation}[^"\\]+)""",
"""value="*(?:function\s)?({command_module}[^\s"\\]+)""",
"""Host\s*Application\s*=\s*({powershell_image}[^\s]+)\s+EngineVersion""",
"""Host\s*Application\s*=\s*({process_command_line}[^\s]+)"""",
"""CommandInvocation(.+?):\s*\\*"({command_invocation}[^"\\]+)""",
"""Details:.+?CommandInvocation.+?ParameterBinding.+?value="(function\s)?({command_module}[^\s,"]+)""",
"""Context[^@]+?User\s*=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))(\\r|\\n|\\t)*\s*(Connected User|Shell ID) ="""
"""Context[^@]+?Host Application\s*=\s*({process_command_line}.+?)(\\r|\\n|\\t)*\s*Engine Version ="""
"""Context[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version =""",
"""Context[^@]+?Command Type\s*=\s*(|({command_type}[^=]+?))(\\r|\\n|\\t)*\s*Script Name ="""
"""Context[^@]+?Command Name\s*=\s*(|({command_name}[^=]+?))(\\r|\\n|\\t)*\s*Command Type ="""
"""Context[^@]+?Script Name\s*=\s+({script_name}\S[^=]+?)\s+Command Path ="""
"""Engine Version\s*=\s*({engine_version}[^\s\\r\\n]+)\s*"""
"""<Level>({run_level}[^<]+)<"""
"""exa_regex=<TimeCreated SystemTime\\*=('|")({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d{3})"""
"""exa_regex=({event_code}4103)"""
"""exa_regex=<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
"""exa_regex=<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""exa_regex=<Execution ProcessID\\*='({process_id}\d+)"""
"""exa_regex=<Security UserID\\*='({user_sid}[\w\-]+)'/>"""
"""exa_regex=User = (({domain}[^=]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)(\\r|\\n|\\t)*\s*(Connected User|Shell ID)\s*=""",
"""exa_regex=CommandInvocation(.+?):\s*"({command_invocation}[^"\\]+)""",
"""exa_regex=value="*(?:function\s)?({command_module}[^\s"\\]+)""",
"""exa_regex=Host\s*Application\s*=\s*({powershell_image}[^\s]+)\s+EngineVersion""",
"""exa_regex=Host\s*Application\s*=\s*({process_command_line}[^\s]+)"""",
"""exa_regex=CommandInvocation(.+?):\s*\\*"({command_invocation}[^"\\]+)""",
"""exa_regex=Details:.+?CommandInvocation.+?ParameterBinding.+?value="(function\s)?({command_module}[^\s,"]+)""",
"""exa_regex=Context[^@]+?User\s*=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))(\\r|\\n|\\t)*\s*(Connected User|Shell ID) ="""
"""exa_regex=Context[^@]+?Host Application\s*=\s*({process_command_line}.+?)(\\r|\\n|\\t)*\s*Engine Version ="""
"""exa_regex=Context[^@]+?Host Application\s*=\s*({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s]+))[^\n]+?\s+Engine Version =""",
"""exa_regex=Context[^@]+?Command Type\s*=\s*(|({command_type}[^=]+?))(\\r|\\n|\\t)*\s*Script Name ="""
"""exa_regex=Context[^@]+?Command Name\s*=\s*(|({command_name}[^=]+?))(\\r|\\n|\\t)*\s*Command Type ="""
"""exa_regex=Context[^@]+?Script Name\s*=\s+({script_name}\S[^=]+?)\s+Command Path ="""
"""exa_regex=Engine Version\s*=\s*({engine_version}[^\s\\r\\n]+)\s*"""
"""exa_regex=<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```