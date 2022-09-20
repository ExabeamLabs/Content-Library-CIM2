#### Parser Content
```Java
{
Name = microsoft-evpowershell-cef-process-create-success-4102
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """|Microsoft-Windows-PowerShell:4102|""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\sduser=(SYSTEM|({user}[^\s]+))\s""",
    """\sahost=({host}[^\s]+)\s""",
    """\sad.ProcessID=({process_id}[^\s]+)\s""",
    """\|Microsoft-Windows-PowerShell:4102\|({additional_info}[^|]+)\|""",
  ]
  ParserVersion = "v1.0.0"


}
```