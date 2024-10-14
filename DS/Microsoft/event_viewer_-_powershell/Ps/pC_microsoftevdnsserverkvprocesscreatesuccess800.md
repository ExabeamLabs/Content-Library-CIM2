#### Parser Content
```Java
{
Name = microsoft-evdnsserver-kv-process-create-success-800
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Windows PowerShell""", """CommandLine=""", """(EventID 800)""", """ScriptName =""", """PowerShell: [""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[^\s]+)\sPowerShell\[""",
    """UserId=({domain}[^\\]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """HostApplication=({powershell_image}[^=]+?)\s+\w+=""",
    """ScriptName =\s*({process_path}({process_dir}[^\s=]+?)({process_name}[^\\=]*?))\s+\w+=""",
    """CommandLine=\s*(|({process_command_line}.+?))\s+\w+:""",
    """Details:[^@]+?CommandInvocationParameterBinding[^@]+?value="+\s*({command_module}[^"]*?)\s*"+""",
    """Details:[^@]+?CommandInvocation\([^\)]+\):\s*\\*"+\s*({command_invocation}[^"\\]+)\s*""",
    """\(EventID ({event_code}800)"""
  ]
  ParserVersion = "v1.0.0"


}
```