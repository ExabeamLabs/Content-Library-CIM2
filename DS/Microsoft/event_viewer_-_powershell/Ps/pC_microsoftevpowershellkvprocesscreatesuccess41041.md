#### Parser Content
```Java
{
Name = microsoft-evpowershell-kv-process-create-success-4104-1
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """eventid="4104"""", """Microsoft-Windows-PowerShell""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[\w\.\-]{1,40}\$?))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
    """({event_name}Creating Scriptblock text)""",
    """ScriptBlock ID:\s+({scriptblock_id}[^\s]+)""",
    """({process_name}PowerShell)""",
    """Creating Scriptblock text\s*\([^\)]+\):\s*({scriptblock_text}.+?)\s*ScriptBlock ID:""",
  ]
  DupFields = ["event_id->event_code"]
  ParserVersion = "v1.0.0"


}
```