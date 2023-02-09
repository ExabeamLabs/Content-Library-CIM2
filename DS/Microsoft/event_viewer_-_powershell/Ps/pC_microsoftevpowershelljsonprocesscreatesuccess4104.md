#### Parser Content
```Java
{
Name = microsoft-evpowershell-json-process-create-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4104""", """Microsoft-Windows-PowerShell[""", """"Category":"""", """"ScriptBlockId":""""  ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"EventID":({event_code}\d+)""",
    """"ProcessID":({process_id}\d+)""",
    """"Domain":"({domain}[^"]+)"""",
    """"AccountName":"({user}[^"]+)"""",
    """"UserID":"({user_sid}[^"]+)"""",
    """"Message":"({event_name}[^\(:]+?)\s*\(""",
    """"ScriptBlockId":"({scriptblock_id}[^"]+)"""",
    """({process_name}PowerShell)"""
  ]
  ParserVersion = "v1.0.0"


}
```