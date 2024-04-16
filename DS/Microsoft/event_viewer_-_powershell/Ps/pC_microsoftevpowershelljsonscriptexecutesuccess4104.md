#### Parser Content
```Java
{
Name = microsoft-evpowershell-json-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"EventID":4104""", """Microsoft-Windows-PowerShell""", """"Category":"""", """"ScriptBlockId":""""  ]
  Fields = [
    """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""",
    """"Hostname":"({host}[^"]+)"""",
    """"EventID":({event_code}\d+)""",
    """"ProcessID":({process_id}\d+)""",
    """"Domain":"({domain}[^"]+)"""",
    """"AccountName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"UserID":"({user_sid}[^"]+)"""",
    """"Message":"({event_name}[^\(:]+?)\s*\(""",
    """"ScriptBlockId":"({scriptblock_id}[^"]+)"""",
    """({process_name}PowerShell)"""
    """"ScriptBlockText":"\s*({scriptblock_text}.+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```