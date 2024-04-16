#### Parser Content
```Java
{
Name = microsoft-evdnsserver-kv-process-create-success-800-1
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Windows PowerShell""", """PowerShell (800)""", """CommandLine=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[+-]\S+\s*({host}\S+)\sEvntSLog""",
    """UserId=({domain}[^\\]*?)\\+(SYSTEM|({user}[\w\.\-]{1,40}\$?))\s+HostName""",
    """Host\s*Application\s*=\s*({powershell_image}[^=]+\.\w+)\s""",
    """ScriptName =\s*({process_path}({process_dir}([\w:]+\\)?([^\\=]+?\\)*?)({process_name}[^\\=]*?))\s+CommandLine=""",
    """CommandLine=\s*({process_command_line}.*?)\s*Details:""",
    """Details:.*?CommandInvocation.*?ParameterBinding.*?value="+\s*({command_module}[^"]*?)\s*"+""",
    """Details:.+?CommandInvocation\(.+?\):\s*\\*"+\s*({command_invocation}[^"\\]+)\s*""",
    """({event_code}800)"""
  ]
  ParserVersion = "v1.0.0"


}
```