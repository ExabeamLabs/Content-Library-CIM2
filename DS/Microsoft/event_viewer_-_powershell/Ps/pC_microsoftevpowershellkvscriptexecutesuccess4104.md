#### Parser Content
```Java
{
Name = microsoft-evpowershell-kv-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
"""4104""",
"""Microsoft-Windows-PowerShell""",
"""Creating Scriptblock text"""
  ]
  Fields = [
    """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}4104)""",
    """AccountName":"(SYSTEM|({user}[^"]+))"""",
    """Domain":"(NT AUTHORITY|({domain}[^"]+))"""",
    """Microsoft-Windows-PowerShell\s+(SYSTEM|NETWORK SERVICE|({user}.+?))\s+User""",
    """ComputerName:\s*({host}[\w.-]+)""",
    """TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """User:\s*({user}.+?)\s*\w+:""",
    """({event_name}Creating Scriptblock text)""",
    """ScriptBlock ID:\s+({scriptblock_id}[^\s"`]+)""",
    """({process_name}PowerShell)""",
    """Process ID:\s*({process_id}\d+)""",
    """Creating Scriptblock text\s*\([^)]+\):\s*({scriptblock_text}.+?)\s*ScriptBlock ID:"""
    """providername="+({provider_name}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
  ]


}
```