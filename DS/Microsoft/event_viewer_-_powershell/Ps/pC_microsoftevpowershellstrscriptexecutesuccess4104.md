#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """Microsoft-Windows-PowerShell (4104)""", """Microsoft-Windows-PowerShell/Operational""" ]
  Fields = [
    """({host}\S+)\s+\S+ - - - \S+\s+\S+\s+({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d{4}):[^\(]+\(({event_code}\d+)\) - \\*"+({script_message}[^:]+):""",
    """ScriptBlock ID:\s+({scriptblock_id}[^\s]+)""",
    """Creating Scriptblock text \([^\)]+\):({scriptblock_text}.+)\s+ScriptBlock ID:""",
    """\(({event_code}4104)\)""",
    """({process_name}PowerShell)"""
  ]
  ParserVersion = "v1.0.0"


}
```