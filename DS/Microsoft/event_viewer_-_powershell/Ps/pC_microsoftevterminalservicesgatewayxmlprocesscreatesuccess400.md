#### Parser Content
```Java
{
Name = "microsoft-evterminalservicesgateway-xml-process-create-success-400"
Vendor = "Microsoft"
Product = "Event Viewer - PowerShell"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""">Windows PowerShell<"""
"""NewEngineState=Available"""
""">400</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z('|")\/>"""
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""\sHostApplication\s*=\s*({process_command_line}({process_path}(({process_dir}\w+:[\\\/]+[^\;=]+)[\\\/]+)?({process_name}[^\s\\\/=]+))[^\n]*?)\s+EngineVersion=""",
"""({event_name}Engine state is changed from None to Available)"""
"""({event_code}\d+)<\/EventID>"""
"""<Keywords>({result}[^<]+)"""
"""<EventRecordID>({event_id}[^<]+)"""
]
ParserVersion = "v1.0.0"


}
```