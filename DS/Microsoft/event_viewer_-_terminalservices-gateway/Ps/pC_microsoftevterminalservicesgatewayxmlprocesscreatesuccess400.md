#### Parser Content
```Java
{
Name = "microsoft-evterminalservicesgateway-xml-process-create-success-400"
Vendor = "Microsoft"
Product = "Event Viewer - TerminalServices-Gateway"
TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
Conditions = [
""">Windows PowerShell<"""
"""<Message>Engine state is changed from None to Available"""
"""Engine Lifecycle"""
""">400</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z'\/>"""
"""<Computer>({host}[^<]+)</Computer>"""
"""\sHostApplication=({process_command_line}({process_name}[^\s\\\/]+)[^\n]*?)\s+EngineVersion="""
"""({event_name}Engine state is changed from None to Available)"""
"""({event_code}\d+)<\/EventID>"""
"""<Keywords>({result}[^<]+)"""
"""<EventRecordID>({event_id}[^<]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```