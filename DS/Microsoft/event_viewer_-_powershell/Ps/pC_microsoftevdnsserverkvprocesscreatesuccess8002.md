#### Parser Content
```Java
{
Name = microsoft-evdnsserver-kv-process-create-success-800-2
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """PowerShell""", """EventID: 800""", """HostApplication""" ]
  Fields = [
    """({host}[\w\-\.]+) PowerShell""",
    """({event_code}800)""",
    """UserId=({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+HostName""",
    """HostApplication=\s*({powershell_image}\S+?)\s+""",
    """CommandLine=\s*({process_command_line}\S[^<]+?)\s+(?:\{\s+)?Details:""",
    """CommandInvocation[^:]+:\s*"({command_invocation}[^"]+)"""",
    """CommandInvocation[^<]*?value="\s*(|-|({command_module}[^"]+?))\s*"\s*"""
    ]
	ParserVersion = "v1.0.0"


}
```