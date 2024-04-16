#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-process-create-success-600"
Vendor = "Microsoft"
Product = "Event Viewer - PowerShell"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""">Windows PowerShell<"""
"""is Started"""
"""<Task>Provider Lifecycle</Task>"""
""">600</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({dest_host}({host}[\w\-.]+))<"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""\sHostApplication\s*=\s*({process_command_line}({process_path}(({process_dir}[^\;=\s]+)[\\\/]+)?({process_name}[^\s\\\/=]+))[^\n]*?)\s+EngineVersion="""
"""<Message>({event_name}[^:=<.]+)\."""
"""({event_code}\d+)<"""
"""<Keywords>({result}[^<]+)"""
"""<EventRecordID>({event_id}[^<]+)"""
"""<Message>({event_name}[^:=<.]+)\."""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```