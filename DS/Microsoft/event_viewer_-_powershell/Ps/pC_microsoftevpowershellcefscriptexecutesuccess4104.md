#### Parser Content
```Java
{
Name = microsoft-evpowershell-cef-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """|Microsoft-Windows-PowerShell:4104|""", """|Creating Scriptblock text""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"UserId"":""({user_sid}.+?)"""",
    """"Computer"":""({host}.+?)"""",
    """"ScriptBlockId"":""({scriptblock_id}.+?)"""",
    """"ScriptBlockText"":""({scriptblock_text}.+?)"""",
    """-Function\s+'({function}[^']+)""",
    """"MessageTotal"":""(|({message_total}.+?))"""",
    """"MessageNumber"":""(|({message_number}.+?))"""",
    """message=({script_message}[^:]+)""",
    """"Path"":""(|({path}.+?))"""",
    """"ProcessID"":""({process_id}\d+)"""",
    """duser=({user}[\w\.\-]{1,40}\$?)""",
  ]
  ParserVersion = "v1.0.0"


}
```