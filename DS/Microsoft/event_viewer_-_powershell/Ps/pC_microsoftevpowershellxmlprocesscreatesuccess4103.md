#### Parser Content
```Java
{
Name = "microsoft-evpowershell-xml-process-create-success-4103"
Vendor = "Microsoft"
Product = "Event Viewer - PowerShell"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""Microsoft-Windows-PowerShell"""
"""Context:"""
"""<Provider Name ="""
"""<EventID>4103<"""
]
Fields = [
"""<TimeCreated SystemTime\\*='({time}\d+\-\d+\-\d+T\d+:\d+:\d+\.\d{3})"""
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
]
ParserVersion = "v1.0.0"


}
```