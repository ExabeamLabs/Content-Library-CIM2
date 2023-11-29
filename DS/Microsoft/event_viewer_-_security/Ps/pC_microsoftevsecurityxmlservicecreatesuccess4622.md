#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-service-create-success-4622"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4622<"""
"""<Provider Name"""
"""Microsoft-Windows-Security-Auditing"""
]
Fields = [
"""({event_code}4622)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({dest_host}({host}[\w\-.]+))"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<Keyword>({result}[^<]+)<\/Keyword>"""
"""<EventRecordID>({event_id}[^<]+)<\/EventRecordID>"""
"""({event_name}A security package has been loaded by the Local Security Authority)"""
"""Message>[^\]\}]*?<Task>({operation}[^<]+?)<"""
"""<Provider Name\\*=('|")Microsoft-Windows-Security-Auditing('|") Guid=('|")\{({process_guid}[^}]+?)\}"""
"""<Correlation ActivityID\\*=('|")\{({activity_id}[^\}'"]+)"""
"""<Execution ProcessID\\*=('|")({process_id}[^'"]+)"""
"""ThreadID\\*=('|")({thread_id}[^'"]+)"""
"""<Provider>({provider_name}[^<]+?)<"""
"""<Data Name\\*=('|")SecurityPackageName('|")>({service_name}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```