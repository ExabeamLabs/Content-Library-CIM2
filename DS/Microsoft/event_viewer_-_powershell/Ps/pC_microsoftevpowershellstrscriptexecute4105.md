#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-script-execute-4105
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ (EventID 4105)""", """ScriptBlock ID:""", """Runspace ID:""", """Microsoft-Windows-PowerShell""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMicrosoft-Windows-PowerShell""",
    """EventID\s({event_code}\d+)""",
    """({provider_name}Microsoft-Windows-PowerShell)\[\d+\]:\s+({domain}[\w\s]+)\\({user}[^:\s]+)""",
    """({event_name}Started invocation of ScriptBlock ID)""",
    """ScriptBlock\sID:\s+({scriptblock_id}[\w\-]+)""",
# runspace_id is removed
  ]



}
```