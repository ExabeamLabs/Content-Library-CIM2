#### Parser Content
```Java
{
Name = microsoft-evpowershell-kv-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "epoch_sec"]
  Conditions = [
"""4104""",
"""Microsoft-Windows-PowerShell""",
"""Creating Scriptblock text"""
  ]
  Fields = [
    """TimeGenerated=({time}\d{10})"""
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)((\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s)?""",
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}4104)""",
    """AccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """Domain"*(:|=)\s*"*({domain}[^=]+?)"*\s+\w+?(:|=)""",
    """Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+User""",
    """ComputerName:\s*({host}[\w.-]+)""",
    """ComputerName =({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s""",
    """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\w+?(:|=)""",
    """({event_name}Creating Scriptblock text)""",
    """ScriptBlock ID:\s+({scriptblock_id}[^\s"`]+)""",
    """({process_name}PowerShell)""",
    """Process ID:\s*({process_id}\d+)""",
    """Creating Scriptblock text\s*\([^)]+\):\s*({scriptblock_text}.+?)\s*ScriptBlock ID:"""
    """providername="+({provider_name}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
    """\susername=\s*(({user_upn}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """OriginatingComputer(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*""",
    """\sLevel(:|=)"*({severity}[^=]+?)"*\s+\w+?(:|=)""",
    """\sTask(:|=)"*({operation}[^=]+?)"*\s+\w+?(:|=)""",
  ]


}
```