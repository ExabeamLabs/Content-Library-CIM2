#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-script-execute-success-4104
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [
"""<EventID>4104<""",
"""ScriptBlockText"""
  ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)('|")""",
    """<Security UserID\\*=('|")(({user_sid}S-[^'"]+?)|(({domain}[^'"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))('|")""",
    """<Computer>({dest_host}({host}[\w\-.]+))<[\\\/]+Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-\.]+)""",
    """<Data Name\\*=('|")ScriptBlockId('|")>({scriptblock_id}[^<]+)<[\\\/]+Data>""",
    """Function\s+('|")({function}[^'"]+)('|")""",
    """<Data Name\\*=('|")MessageTotal('|")>({message_total}\d+)""",
    """<Data Name\\*=('|")MessageNumber('|")>({message_number}\d+)""",
    """<Message>({script_message}[^:]+)""",
    """<Data Name\\*=('|")Path('|")>({path}[^<]+)<[\\\/]+Data>""",
    """<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """({event_code}4104)""",
    """({event_name}Creating Scriptblock text)""",
    """({process_name}PowerShell)""",
    """<Data Name\\*=('|")ScriptBlockText('|")>\s*({scriptblock_text}[^<]+?)\s*<[\\\/]+Data>""",
    """"ScriptBlockText":"({scriptblock_text}[^"]+?)\s*""""
    """<Level>({run_level}[^<]+)<""",
    """<Channel>({channel}[^<]+?)<""",
    """<Keywords>({result}[^<]+?)<""",
    """<EventRecordID>({event_id}[^<]+?)<""",
    """<Task>({operation}[^<]+?)<""",
    """<Opcode>({opcode}[^<]+?)<""",
    """exa_regex=<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)('|")""",
    """exa_regex=<Security UserID\\*=('|")(({user_sid}S-[^'"]+?)|(({domain}[^'"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))('|")""",
    """exa_regex=<Computer>({dest_host}({host}[\w\-.]+))<[\\\/]+Computer>""",
    """exa_regex=<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-\.]+)""",
    """exa_regex=<Data Name\\*=('|")ScriptBlockId('|")>({scriptblock_id}[^<]+)<[\\\/]+Data>""",
    """exa_regex=Function\s+('|")({function}[^'"]+)('|")""",
    """exa_regex=<Data Name\\*=('|")MessageTotal('|")>({message_total}\d+)""",
    """exa_regex=<Data Name\\*=('|")MessageNumber('|")>({message_number}\d+)""",
    """exa_regex=<Message>({script_message}[^:]+)""",
    """exa_regex=<Data Name\\*=('|")Path('|")>({path}[^<]+)<[\\\/]+Data>""",
    """exa_regex=<Execution ProcessID\\*=('|")({process_id}\d+)""",
    """exa_regex=({event_code}4104)""",
    """exa_regex=({event_name}Creating Scriptblock text)""",
    """exa_regex=({process_name}PowerShell)""",
    """exa_regex=<Data Name\\*=('|")ScriptBlockText('|")>\s*({scriptblock_text}[^<]+?)\s*<[\\\/]+Data>""",
    """exa_regex="ScriptBlockText":"({scriptblock_text}[^"]+?)\s*""""
    """exa_regex=<Level>({run_level}[^<]+)<"""
]


}
```