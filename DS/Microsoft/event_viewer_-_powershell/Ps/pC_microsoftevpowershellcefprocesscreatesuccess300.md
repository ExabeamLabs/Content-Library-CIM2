#### Parser Content
```Java
{
Name = microsoft-evpowershell-cef-process-create-success-300
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "epoch"]
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """PowerShell:300|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
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
    """-file\s({process_path}({process_dir}[^\s]+\\\\({process_name}[^\s\\]+)))""",
    """CommandLine\\*=({process_command_line}[^\s]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```