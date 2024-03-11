#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
"""<EventID>4104<""",
"""Microsoft-Windows-PowerShell""",
"""ScriptBlockText"""
  ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'""",
    """<Security UserID='({user_sid}[^']+)""",
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<Data Name ='ScriptBlockId'>({scriptblock_id}[^<]+)</Data>""",
    """Function\s+'({function}[^']+)""",
    """<Data Name ='MessageTotal'>({message_total}\d+)""",
    """<Data Name ='MessageNumber'>({message_number}\d+)""",
    """<Message>({script_message}[^:]+)""",
    """<Data Name ='Path'>({path}[^<]+)</Data>""",
    """<Execution ProcessID='({process_id}\d+)""",
    """({event_code}4104)""",
    """({event_name}Creating Scriptblock text)""",
    """({process_name}PowerShell)""",
    """<Data Name ='ScriptBlockText'>\s*({scriptblock_text}[^<]+?)\s*<\/Data>""",
    """"ScriptBlockText":"({scriptblock_text}[^"]+?)\s*""""
]
  DupFields = [ "host->dest_host" ]


}
```